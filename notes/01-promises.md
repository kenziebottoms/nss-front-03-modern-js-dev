## Basic Promises

Below is a basic pass/fail promise.

```Javascript
const promisedAjax = () => {
    return new Promise((resolve, reject) => {
        $.ajax({
            url: "url.com"
        }).done(results => resolve(results))
        .fail(error => reject(error));
    });
};

promisedAjax().then(results => {
    // what to do with results (results)
    // upon successful completion (done())
}).catch(error => {
    // what to do with error message (error)
    // upon failure (fail())
});
```