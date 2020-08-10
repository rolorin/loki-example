# Like the God of Mischief, mocking your APIs

---

## Directory Structure

---

- functions, holds lambda functions.
- mocks, contains url path as sub directories.
  - example GET /vendors response will be in mocks/get/vendors
  - response.json contains
    ```
    {
        "latency": { // These values are used to create artificial latency for API
            "p95": "some int value",
            "p99": "another int value"
        },
        "response": {} // actual API response
    }
    ```
- responders, contains jsonReader
- utility, contains helpers
  - utility/latencyCalculator, calculates latency from p95, p99

## WIP Status

- Only put handler works for now with hard coded response.
- The latency of the APIs is not 100% reliable.
