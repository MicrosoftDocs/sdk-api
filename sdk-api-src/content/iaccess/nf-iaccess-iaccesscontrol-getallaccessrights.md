---
UID: NF:iaccess.IAccessControl.GetAllAccessRights
title: IAccessControl::GetAllAccessRights
author: windows-sdk-content
description: Gets the entire list of access rights and/or the owner and group for the specified object.
old-location: com\iaccesscontrol_getallaccessrights.htm
tech.root: com
ms.assetid: 8c8551fb-8ba9-4a52-b6f8-bd11e4006fe9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAllAccessRights, GetAllAccessRights method [COM], GetAllAccessRights method [COM],IAccessControl interface, IAccessControl interface [COM],GetAllAccessRights method, IAccessControl.GetAllAccessRights, IAccessControl::GetAllAccessRights, _com_iaccesscontrol_getallaccessrights, com.iaccesscontrol_getallaccessrights, iaccess/IAccessControl::GetAllAccessRights
ms.topic: method
req.header: iaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IAccess.h
api_name:
 - IAccessControl.GetAllAccessRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

