# PBI-Issue2
Another issue with ADLSg2 and incremental load

Create a storage account in the same region as your PBI region.

Deploy *Example.pbit* to a Pro workspace
Confirm it refreshes ok

Deploy *ExampleWithIncrementalLoading.pbit* to Pro workspace
Confirm the refresh fails

> ## Something went wrong
>
> There was an error when processing the data in the dataset.
> Please try again later or contact support. If you contact support, please provide these details.
> MessageResource name and Location need to match. Resource name: ListFiles. Location: Polling_...

If you deploy to a Premium workspace the incremental load will work.

Incremental loading is now GA for Pro workspaces - https://powerbi.microsoft.com/en-us/blog/incremental-refresh-is-generally-available/

Notes:
At first I thought this was some undocumented restriction as our storage accounts were LRS and bizarrely the PBI tenant was in a different region to our Azure infrastructure.
