SET( APP_LIST
  comparegui
  comparesimple
)

FOREACH( var ${APP_LIST} )
  ADD_EXECUTABLE( ${var}
    ${var}.cxx
    )

  TARGET_LINK_LIBRARIES( ${var}
    QGoGui
    )

  INSTALL( TARGETS ${var}
    RUNTIME DESTINATION ${QGOIMAGECOMPARE_INSTALL_BIN_DIR} COMPONENT Runtime
    BUNDLE  DESTINATION ${QGOIMAGECOMPARE_INSTALL_BUNDLE_DIR} COMPONENT Runtime
    ARCHIVE DESTINATION ${QGOIMAGECOMPARE_INSTALL_LIB_DIR} COMPONENT Libraries
    LIBRARY DESTINATION ${QGOIMAGECOMPARE_INSTALL_LIB_DIR} COMPONENT Libraries
    )

ENDFOREACH( var ${APP_LIST} )
