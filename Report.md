## Integration Testing
Integration Test also known as  'I & T' (Integration and Testing), 'String Testing' and sometimes 'Thread Testing',is  defined as a type of testing where software modules are integrated logically and tested as a group.  The purpose of this level of testing is to expose defects in the interaction between the software modules when they are integrated

## Integration Test vs Unit Test

* Unit testing verifies that each component of the program is functional, whereas integration testing integrates many application modules and tests them collectively to ensure that they are all functioning properly.
* While integration testing begins with interface specification, unit testing begins with module specification.
* While integration testing is done after unit testing and before system testing, unit testing can be done at any time.

## Implementation
```
    RestTemplate restTemplate = new RestTemplate();
    ResponseEntity<String> response = restTemplate.getForEntity(url, String.class);

    assertNotNull(response);
    assertTrue(response.getStatusCode() == HttpStatus.OK);
    assertEquals(MediaType.APPLICATION_JSON, response.getHeaders().getContentType());
    assertTrue(isValid(response.getBody()));
```

We obtained the API answer and used it in the code sample. Then we verified that it is not null, the response status code is OK, the content is JSON, and the JSON is correct. Using this technique, the compatibility of our code is validated with REST API.

## SETUP
The following commands can be run to get result of IT
```
    chmod +x gradlew
    ./gradlew build
    ./gradlew test
```

[//]: # (## TEST RESULTS)

[//]: # (![result]&#40;./TestResult.png&#41;)
