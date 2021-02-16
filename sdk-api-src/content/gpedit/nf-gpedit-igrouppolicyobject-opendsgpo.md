---
UID: NF:gpedit.IGroupPolicyObject.OpenDSGPO
title: IGroupPolicyObject::OpenDSGPO (gpedit.h)
description: The OpenDSGPO method opens the specified GPO and optionally loads the registry information.
helpviewer_keywords: ["GPO_OPEN_LOAD_REGISTRY","GPO_OPEN_READ_ONLY","IGroupPolicyObject interface [Group Policy]","OpenDSGPO method","IGroupPolicyObject.OpenDSGPO","IGroupPolicyObject::OpenDSGPO","OpenDSGPO","OpenDSGPO method [Group Policy]","OpenDSGPO method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_opendsgpo","gpedit/IGroupPolicyObject::OpenDSGPO","policy.igrouppolicyobject_opendsgpo"]
old-location: policy\igrouppolicyobject_opendsgpo.htm
tech.root: Policy
ms.assetid: 362b6229-d73f-424f-b906-05ed43e5e034
ms.date: 12/05/2018
ms.keywords: GPO_OPEN_LOAD_REGISTRY, GPO_OPEN_READ_ONLY, IGroupPolicyObject interface [Group Policy],OpenDSGPO method, IGroupPolicyObject.OpenDSGPO, IGroupPolicyObject::OpenDSGPO, OpenDSGPO, OpenDSGPO method [Group Policy], OpenDSGPO method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_opendsgpo, gpedit/IGroupPolicyObject::OpenDSGPO, policy.igrouppolicyobject_opendsgpo
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGroupPolicyObject::OpenDSGPO
 - gpedit/IGroupPolicyObject::OpenDSGPO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.OpenDSGPO
---

# IGroupPolicyObject::OpenDSGPO


## -description

The
    <b>OpenDSGPO</b> method opens the specified GPO and optionally loads the registry information.

## -parameters

### -param pszPath [in]

Specifies the Active Directory path of the object to open. If the path specifies a domain controller, the GPO is created on that DC. Otherwise, the system will select a DC on the caller's behalf.

### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To create a new GPO in the Active Directory, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-new">New</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-new">New</a>