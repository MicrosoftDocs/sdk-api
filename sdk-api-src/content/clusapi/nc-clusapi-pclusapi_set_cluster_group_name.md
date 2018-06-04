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

# PCLUSAPI_SET_CLUSTER_GROUP_NAME callback function


## -description


Sets the name for a  <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>. The <b>PCLUSAPI_SET_CLUSTER_GROUP_NAME</b> type defines a pointer to this function.


## -parameters




### -param hGroup [in]

Handle to the group to name.


### -param lpszGroupName [in]

Pointer to the new name for the group identified by <i>hGroup</i>.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



<i>SetClusterGroupName</i> changes the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> common property of the group identified by 
    <i>hGroup</i>. This is the only way that Name, a read-only property, can be changed.

Do not call <i>SetClusterGroupName</i> from a 
    resource DLL. For more information, see 
    <a href="https://msdn.microsoft.com/0eaa4aea-8d9a-4552-b43a-fafa23a3e736">Function Calls to Avoid in Resource DLLs</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>



<a href="https://msdn.microsoft.com/0c7ef9d9-d32b-448e-9e07-6befb9b3e338">OpenClusterGroup</a>
 

 

