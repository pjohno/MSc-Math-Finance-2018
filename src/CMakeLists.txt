
SET(MY_LIBRARY_SRCS  
MSc_projects_pde_solvers.cpp
MSc_projects_quad.cpp
MSc_projects_perpetual_bermudan_put.cpp
)

ADD_LIBRARY( mscmathfinanceprojects SHARED
${MY_LIBRARY_SRCS} 
)

TARGET_LINK_LIBRARIES( mscmathfinanceprojects math60082 boost_system pthread gsl cblas)

ADD_LIBRARY( mscmathfinanceprojects_static STATIC
${MY_LIBRARY_SRCS} 
)

TARGET_LINK_LIBRARIES( mscmathfinanceprojects_static math60082_static boost_system pthread gsl cblas)

