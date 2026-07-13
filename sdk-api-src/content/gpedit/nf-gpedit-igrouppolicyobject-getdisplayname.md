---
UID: NF:gpedit.IGroupPolicyObject.GetDisplayName
title: IGroupPolicyObject::GetDisplayName (gpedit.h)
description: The GetDisplayName method retrieves the display name for the GPO. (IGroupPolicyObject.GetDisplayName)
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [Group Policy]","GetDisplayName method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetDisplayName method","IGroupPolicyObject.GetDisplayName","IGroupPolicyObject::GetDisplayName","_win32_igrouppolicyobject_getdisplayname","gpedit/IGroupPolicyObject::GetDisplayName","policy.igrouppolicyobject_getdisplayname"]
old-location: policy\igrouppolicyobject_getdisplayname.htm
tech.root: Policy
ms.assetid: a16592c3-8fa1-4859-b379-ef31999a3fdd
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Group Policy], GetDisplayName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetDisplayName method, IGroupPolicyObject.GetDisplayName, IGroupPolicyObject::GetDisplayName, _win32_igrouppolicyobject_getdisplayname, gpedit/IGroupPolicyObject::GetDisplayName, policy.igrouppolicyobject_getdisplayname
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
 - IGroupPolicyObject::GetDisplayName
 - gpedit/IGroupPolicyObject::GetDisplayName
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
 - IGroupPolicyObject.GetDisplayName
---

# IGroupPolicyObject::GetDisplayName


## -description

The
    <b>GetDisplayName</b> method retrieves the display name for the GPO.

## -parameters

### -param pszName [out]

Pointer to a buffer that receives the display name.

### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To set the display name for a GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setdisplayname">SetDisplayName</a> method. Call 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getname">GetName</a> to retrieve the unique name for a GPO, which is a GUID for an Active Directory object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getname">GetName</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setdisplayname">SetDisplayName</a>
