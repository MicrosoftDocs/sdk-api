---
UID: NF:gpedit.IGroupPolicyObject.GetMachineName
title: IGroupPolicyObject::GetMachineName (gpedit.h)
description: The GetMachineName method retrieves the computer name of the remote GPO. This is the name specified by the OpenRemoteMachineGPO method.
helpviewer_keywords: ["GetMachineName","GetMachineName method [Group Policy]","GetMachineName method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetMachineName method","IGroupPolicyObject.GetMachineName","IGroupPolicyObject::GetMachineName","_win32_igrouppolicyobject_getmachinename","gpedit/IGroupPolicyObject::GetMachineName","policy.igrouppolicyobject_getmachinename"]
old-location: policy\igrouppolicyobject_getmachinename.htm
tech.root: Policy
ms.assetid: 6ac20718-45d4-4a45-a95e-d159e4d6dacc
ms.date: 12/05/2018
ms.keywords: GetMachineName, GetMachineName method [Group Policy], GetMachineName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetMachineName method, IGroupPolicyObject.GetMachineName, IGroupPolicyObject::GetMachineName, _win32_igrouppolicyobject_getmachinename, gpedit/IGroupPolicyObject::GetMachineName, policy.igrouppolicyobject_getmachinename
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
 - IGroupPolicyObject::GetMachineName
 - gpedit/IGroupPolicyObject::GetMachineName
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
 - IGroupPolicyObject.GetMachineName
---

# IGroupPolicyObject::GetMachineName


## -description

The
    <b>GetMachineName</b> method retrieves the computer name of the remote GPO. This is the name specified by the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openremotemachinegpo">OpenRemoteMachineGPO</a> method.

## -parameters

### -param pszName [out]

Pointer to a buffer that receives the computer name.

### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openremotemachinegpo">OpenRemoteMachineGPO</a>