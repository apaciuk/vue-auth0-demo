<template>
  <div>
    <h1>External API</h1>
    <p>
      You use will use a button to call an external API using an access token,
      and the API will validate it using the API's audience value.
      <br />
      <strong>This route should be protected</strong>.
    </p>
    <div
      class="btn-group mt-5"
      role="group"
      aria-label="External API Requests Examples"
    >
      <button type="button" class="btn btn-primary">Get Public Message</button>
      <button type="button" class="btn btn-primary">
        Get Protected Message
      </button>
    </div>

    <div v-if="message" class="mt-5">
      <h6 class="muted">Result</h6>
      <div class="container-fluid">
        <div class="row">
          <code class="col-12 text-light bg-dark p-4">
            {{ JSON.stringify(message, null, 2) }}
          </code>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ExternalApi",
  data() {
    return {
      message: null,
    };
  },
};
</script>
