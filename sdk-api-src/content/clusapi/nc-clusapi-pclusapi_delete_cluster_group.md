---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PCLUSAPI_DELETE_CLUSTER_GROUP callback function


## -description


Removes an offline and empty 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> from a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>. The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to be removed. You must close this handle separately.


## -returns



This function returns a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. If the 
       operation completes successfully the function returns <b>ERROR_SUCCESS</b> (0). Any other 
       returned system error code would indicate that the 
       operation failed.




## -remarks



The <b>PCLUSAPI_DELETE_CLUSTER_GROUP</b> type defines a pointer to this function.

Because the <i>DeleteClusterGroup</i> function only 
     removes groups that are empty, a group must not have any 
     <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> if it is to be successfully deleted. To delete a group 
     with resources, use the <a href="https://msdn.microsoft.com/ac293d5b-edc8-4c5f-9b05-9e2349bf1453">DestroyClusterGroup</a> 
     function.

<i>DeleteClusterGroup</i> does not close the group 
     handle specified by <i>hGroup</i>. To avoid memory leaks, be sure to close this handle with 
     <a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>.

Do not call <i>DeleteClusterGroup</i> from a resource 
     DLL. For more information, see 
     <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/5bbacf45-2e1a-402a-8592-c8f60034c4ad">CloseClusterGroup</a>



<a href="https://msdn.microsoft.com/7011640e-87d0-4f2b-971c-9e86c77db13e">CreateClusterGroup</a>



<a href="https://msdn.microsoft.com/ac293d5b-edc8-4c5f-9b05-9e2349bf1453">DestroyClusterGroup</a>



<a href="https://msdn.microsoft.com/a2336594-ac24-476e-94e8-460a31c1f643">Group Management Functions</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

