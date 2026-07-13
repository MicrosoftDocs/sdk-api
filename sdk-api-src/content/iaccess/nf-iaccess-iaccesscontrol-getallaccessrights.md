---
UID: NF:iaccess.IAccessControl.GetAllAccessRights
title: IAccessControl::GetAllAccessRights (iaccess.h)
description: Gets the entire list of access rights and/or the owner and group for the specified object.
helpviewer_keywords: ["GetAllAccessRights","GetAllAccessRights method [COM]","GetAllAccessRights method [COM]","IAccessControl interface","IAccessControl interface [COM]","GetAllAccessRights method","IAccessControl.GetAllAccessRights","IAccessControl::GetAllAccessRights","_com_iaccesscontrol_getallaccessrights","com.iaccesscontrol_getallaccessrights","iaccess/IAccessControl::GetAllAccessRights"]
old-location: com\iaccesscontrol_getallaccessrights.htm
tech.root: com
ms.assetid: 8c8551fb-8ba9-4a52-b6f8-bd11e4006fe9
ms.date: 12/05/2018
ms.keywords: GetAllAccessRights, GetAllAccessRights method [COM], GetAllAccessRights method [COM],IAccessControl interface, IAccessControl interface [COM],GetAllAccessRights method, IAccessControl.GetAllAccessRights, IAccessControl::GetAllAccessRights, _com_iaccesscontrol_getallaccessrights, com.iaccesscontrol_getallaccessrights, iaccess/IAccessControl::GetAllAccessRights
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessControl::GetAllAccessRights
 - iaccess/IAccessControl::GetAllAccessRights
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IAccess.h
api_name:
 - IAccessControl.GetAllAccessRights
---

# IAccessControl::GetAllAccessRights


## -description

Gets the entire list of access rights and/or the owner and group for the specified object.

## -parameters

### -param lpProperty [in]

The name of the property. If you are using the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this parameter must be <b>NULL</b>.

### -param ppAccessList [out]

The address of the pointer variable that receives a pointer to the access list structure. This parameter cannot be [ACTRL_ACCESS](../accctrl/ns-accctrl-explicit_access_a.md).

If the call succeeds, the caller must free the allocated memory with the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. Note that the memory is allocate(all_nodes), which means that all the substructures are allocated in one block. Therefore, the entire data structure must be freed by a single call to <b>CoTaskMemFree</b>.

### -param ppOwner [out]

A pointer to a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that receives the owner information. If this parameter is not <b>NULL</b> and the function succeeds, the caller must free the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param ppGroup [out]

A pointer to a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that receives the group information. If this parameter is not <b>NULL</b> and the function succeeds, the caller must free the memory with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

[ACTRL_ACCESS](../accctrl/ns-accctrl-explicit_access_a.md)



<a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>