# promise
Create three different APIs (or mock functions) that return promises with varying response times. One resolves immediately, one after 2 seconds, and one after 5 seconds. Implement the following using these promises: Promise.all: Fetch all data simultaneously and resolve only when all promises are completed. Promise.race:  

Explanation of Promise.all, Promise.race, and Promise.any:
Promise.all:
What it does: This method takes an array of promises and resolves only when all of the promises in the array have resolved. If any of the promises fail (i.e., reject), Promise.all will reject immediately, even if other promises are still pending or have resolved.
Use case: Use Promise.all when you need all results to be available before proceeding. For example, fetching data from multiple APIs that together provide the complete picture of information you need.
Example: Fetching user data from different endpoints (e.g., profile, posts, friends), and you need all of them to display a full user page.
Promise.race:
What it does: Promise.race resolves or rejects as soon as the first promise in the array settles (either resolves or rejects). Whichever promise completes first, its result is returned, and all other promises are ignored.
Use case: Promise.race is useful when you want to act as soon as the first result is available. For example, in a scenario where you're making a request to multiple servers and you only care about getting the fastest response.
Example: A situation where you query multiple CDNs for an image, and you want to display it as soon as one of the servers responds (ignoring the slower ones).
Promise.any:
What it does: This method resolves as soon as the first successfully resolved promise is returned. It will only reject if all promises fail. Unlike Promise.race, it ignores promises that reject and waits for the first successful result.
Use case: Promise.any is helpful when you’re making several requests and are only concerned about the first successful response, while ignoring any failures from other promises.
Example: Querying different backup APIs or servers, and you only care about the first one that responds successfully, while ignoring any failures or errors from the others.
Key Differences:
Promise.all waits for all promises to settle. If one fails, the entire operation fails.
Promise.race resolves as soon as the first promise (either success or failure) settles.
Promise.any resolves as soon as the first successful promise settles, ignoring rejected ones.
Summary:
Use Promise.all when you need all tasks to be completed before proceeding.
Use Promise.race when you want the first result, regardless of whether it resolves or rejects.
Use Promise.any when you want the first successful result, while ignoring failures.

