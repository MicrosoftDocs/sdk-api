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

# IAccessControl::GetAllAccessRights


## -description


Gets the entire list of access rights and/or the owner and group for the specified object.


## -parameters




### -param lpProperty [in]

The name of the property. If you are using the COM implementation of <a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>, this parameter must be <b>NULL</b>.


### -param ppAccessList [out]

The address of the pointer variable that receives a pointer to the access list structure. This parameter cannot be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/d7fb10c1-ebb8-44cf-b61c-a70a787b324f">ACTRL_ACCESS</a>.

If the call succeeds, the caller must free the allocated memory with the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function. Note that the memory is allocate(all_nodes), which means that all the substructures are allocated in one block. Therefore, the entire data structure must be freed by a single call to <b>CoTaskMemFree</b>.


### -param ppOwner [out]

A pointer to a <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that receives the owner information. If this parameter is not <b>NULL</b> and the function succeeds, the caller must free the memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param ppGroup [out]

A pointer to a <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that receives the group information. If this parameter is not <b>NULL</b> and the function succeeds, the caller must free the memory with <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d7fb10c1-ebb8-44cf-b61c-a70a787b324f">ACTRL_ACCESS</a>



<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>
 

 

