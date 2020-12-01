---
UID: NF:gpedit.IGroupPolicyObject.GetPath
title: IGroupPolicyObject::GetPath (gpedit.h)
description: The GetPath method retrieves the path to the GPO.
helpviewer_keywords: ["GetPath","GetPath method [Group Policy]","GetPath method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetPath method","IGroupPolicyObject.GetPath","IGroupPolicyObject::GetPath","_win32_igrouppolicyobject_getpath","gpedit/IGroupPolicyObject::GetPath","policy.igrouppolicyobject_getpath"]
old-location: policy\igrouppolicyobject_getpath.htm
tech.root: Policy
ms.assetid: ecfecaa4-eb6e-4de6-a5fe-ecd0e9df886c
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [Group Policy], GetPath method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetPath method, IGroupPolicyObject.GetPath, IGroupPolicyObject::GetPath, _win32_igrouppolicyobject_getpath, gpedit/IGroupPolicyObject::GetPath, policy.igrouppolicyobject_getpath
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
 - IGroupPolicyObject::GetPath
 - gpedit/IGroupPolicyObject::GetPath
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
 - IGroupPolicyObject.GetPath
---

# IGroupPolicyObject::GetPath


## -description

The
    <b>GetPath</b> method retrieves the path to the GPO.

## -parameters

### -param pszPath [out]

Pointer to a buffer that receives the path. If the GPO is an Active Directory object, the path is in ADSI name format. If the GPO is a computer object, this parameter receives a file system path.

### -param cchMaxLength [in]

Specifies the maximum number of characters that can be stored in the <i>pszPath</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getdspath">GetDSPath</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>