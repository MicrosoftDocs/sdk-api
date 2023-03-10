---
UID: NF:gpedit.IGroupPolicyObject.SetDisplayName
title: IGroupPolicyObject::SetDisplayName (gpedit.h)
description: The SetDisplayName method sets the display name for the GPO.
helpviewer_keywords: ["IGroupPolicyObject interface [Group Policy]","SetDisplayName method","IGroupPolicyObject.SetDisplayName","IGroupPolicyObject::SetDisplayName","SetDisplayName","SetDisplayName method [Group Policy]","SetDisplayName method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_setdisplayname","gpedit/IGroupPolicyObject::SetDisplayName","policy.igrouppolicyobject_setdisplayname"]
old-location: policy\igrouppolicyobject_setdisplayname.htm
tech.root: Policy
ms.assetid: 979e8399-83e1-421e-8f32-813464ac97aa
ms.date: 12/05/2018
ms.keywords: IGroupPolicyObject interface [Group Policy],SetDisplayName method, IGroupPolicyObject.SetDisplayName, IGroupPolicyObject::SetDisplayName, SetDisplayName, SetDisplayName method [Group Policy], SetDisplayName method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_setdisplayname, gpedit/IGroupPolicyObject::SetDisplayName, policy.igrouppolicyobject_setdisplayname
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
 - IGroupPolicyObject::SetDisplayName
 - gpedit/IGroupPolicyObject::SetDisplayName
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
 - IGroupPolicyObject.SetDisplayName
---

# IGroupPolicyObject::SetDisplayName


## -description

The
    <b>SetDisplayName</b> method sets the display name for the GPO.

## -parameters

### -param pszName [in]

Specifies the new display name.

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