# Karate_demo 
1. Spec is huge, so:
- prioritization will play a big role
- will definetly take more than 1 qa to test all of it, therefore coordination between team members will be my second concern.
- release cycles and cicd. test automation has to be properly architected to avoid creating bottlenecks during release cycles

Functional side documented very well, however, same can't be said about performance requirements. I'd be concerned about lack on info overthere.

2. Spec overview, scenario development, scenario review with a team, manual execution, test automation development, pluging test automation into cicd

3. Usually, I approach web service testing with following scenarios:
- valid request
- invalid request
- fault tolerance

Valid/Invalid requests scenarios are straigt forward. They consists of request generation by levereging all possible data entry points such as headers, path parameters, query parameter and body. And runing asserions over response status code, headers, body (schema or specific properties). To come up with useful test data, I focus on value format, boundary conditions, enum values, optional request data entry points.

Fault tolerance usually covers downstream service failure or network instability tests. Those require brining web service into fault state. It's debatable whether those should be automated, since they require special environment setup.

On top of usual scenarios described above, I'd focus on authentification, http redirects and pagination and json-p callbacks. Such functionalities require more sophisticated scenarios to test them.

4. Postman - manual testing. java + restasured for test automation ,karate.
