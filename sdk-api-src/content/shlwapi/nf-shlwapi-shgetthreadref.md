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

# SHGetThreadRef function


## -description


Retrieves the per-thread object reference set by <a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>.


## -parameters




### -param ppunk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The address of a pointer that, when this function returns successfully, points to the object whose reference is stored. Your application is responsible for freeing this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the object reference exists, or <b>E_NOINTERFACE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/2140e396-29cd-4665-b684-337170570b73">SHCreateThread</a>



<a href="https://msdn.microsoft.com/6abca2df-832c-410b-93c7-5131e481e595">SHCreateThreadRef</a>



<a href="https://msdn.microsoft.com/7f3fd09b-baad-4019-a060-c68727aee61f">SHReleaseThreadRef</a>



<a href="https://msdn.microsoft.com/1d0d70ca-a0e6-4620-9a01-8d4986990b9c">SHSetThreadRef</a>
 

 

