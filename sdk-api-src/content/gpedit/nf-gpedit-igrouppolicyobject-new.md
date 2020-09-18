---
UID: NF:gpedit.IGroupPolicyObject.New
title: IGroupPolicyObject::New (gpedit.h)
description: The New method creates a new GPO in the Active Directory with the specified display name. The method opens the GPO using the OpenDSGPO method.
helpviewer_keywords: ["GPO_OPEN_LOAD_REGISTRY","GPO_OPEN_READ_ONLY","IGroupPolicyObject interface [Group Policy]","New method","IGroupPolicyObject.New","IGroupPolicyObject::New","New","New method [Group Policy]","New method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_new","gpedit/IGroupPolicyObject::New","policy.igrouppolicyobject_new"]
old-location: policy\igrouppolicyobject_new.htm
tech.root: Policy
ms.assetid: e251cac2-8fc8-4ed0-b940-4a9f47eca26b
ms.date: 12/05/2018
ms.keywords: GPO_OPEN_LOAD_REGISTRY, GPO_OPEN_READ_ONLY, IGroupPolicyObject interface [Group Policy],New method, IGroupPolicyObject.New, IGroupPolicyObject::New, New, New method [Group Policy], New method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_new, gpedit/IGroupPolicyObject::New, policy.igrouppolicyobject_new
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
 - IGroupPolicyObject::New
 - gpedit/IGroupPolicyObject::New
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
 - IGroupPolicyObject.New
---

# IGroupPolicyObject::New


## -description

The
    <b>New</b> method creates a new GPO in the Active Directory with the specified display name. The method opens the GPO using the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-opendsgpo">OpenDSGPO</a> method.

## -parameters

### -param pszDomainName [in]

Specifies the Active Directory path of the object to create. If the path specifies a domain controller, the GPO is created on that DC. Otherwise, the system will select a DC on the caller's behalf.

### -param pszDisplayName [in]

Specifies the display name of the object to create.

### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To open a GPO that already exists, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-opendsgpo">OpenDSGPO</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-opendsgpo">OpenDSGPO</a>