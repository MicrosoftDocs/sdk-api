---
UID: NF:gpedit.IGroupPolicyObject.GetName
title: IGroupPolicyObject::GetName (gpedit.h)
description: The GetName method retrieves the unique GPO name.
helpviewer_keywords: ["GetName","GetName method [Group Policy]","GetName method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetName method","IGroupPolicyObject.GetName","IGroupPolicyObject::GetName","_win32_igrouppolicyobject_getname","gpedit/IGroupPolicyObject::GetName","policy.igrouppolicyobject_getname"]
old-location: policy\igrouppolicyobject_getname.htm
tech.root: Policy
ms.assetid: 1374c01c-aba3-48f5-8a42-7139873d8f7c
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Group Policy], GetName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetName method, IGroupPolicyObject.GetName, IGroupPolicyObject::GetName, _win32_igrouppolicyobject_getname, gpedit/IGroupPolicyObject::GetName, policy.igrouppolicyobject_getname
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
 - IGroupPolicyObject::GetName
 - gpedit/IGroupPolicyObject::GetName
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
 - IGroupPolicyObject.GetName
---

# IGroupPolicyObject::GetName


## -description

The
    <b>GetName</b> method retrieves the unique GPO name.

For Active Directory policy objects, the method returns a GUID. For a local GPO, the method returns the string "Local". For remote objects, 
<b>GetName</b> returns the computer name.

## -parameters

### -param pszName [out]

Pointer to a buffer that receives the GPO name.

### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To retrieve the display name for a GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getdisplayname">GetDisplayName</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getdisplayname">GetDisplayName</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>