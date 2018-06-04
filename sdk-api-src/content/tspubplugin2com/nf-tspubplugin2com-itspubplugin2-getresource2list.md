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

# ItsPubPlugin2::GetResource2List


## -description


Retrieves a list of resources assigned to the specified user. The RemoteApp and Desktop Connection Management service calls this method in the following situations:
<ul>
<li>When the user has no cache in Remote Desktop Web Access (RD Web Access).</li>
<li>When the user has a cache, but it has expired.</li>
<li>When a call to <a href="https://msdn.microsoft.com/66b18c7f-2623-44ed-8cb9-3cceaa9bab34">GetCacheLastUpdateTime</a> returns a time that is later than the time stored in the user's cache.</li>
</ul>

## -parameters




### -param userID [in]

A null-terminated string that contains the security identifier (SID) of the user. If this parameter is <b>NULL</b>, this method should return the resources for all users.


### -param pceAppListSize [out]

The address of a <b>LONG</b> variable that receives the number of elements in the <i>resourceList</i> array.


### -param resourceList [out]

The address of an array of <a href="https://msdn.microsoft.com/BD4761C7-377C-499C-B984-3B126C704089">pluginResource2</a> structures that contains the resources for the specified user. You must use the <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> function to allocate this memory. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1ef27b3a-b897-4757-803d-d3a18959895c">ItsPubPlugin2</a>
 

 

