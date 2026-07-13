---
UID: NF:gpedit.IGroupPolicyObject.Delete
title: IGroupPolicyObject::Delete (gpedit.h)
description: The Delete method deletes the GPO.
helpviewer_keywords: ["Delete","Delete method [Group Policy]","Delete method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","Delete method","IGroupPolicyObject.Delete","IGroupPolicyObject::Delete","_win32_igrouppolicyobject_delete","gpedit/IGroupPolicyObject::Delete","policy.igrouppolicyobject_delete"]
old-location: policy\igrouppolicyobject_delete.htm
tech.root: Policy
ms.assetid: 34afb04e-47f9-4d7c-9fa6-9d76188d7e05
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Group Policy], Delete method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],Delete method, IGroupPolicyObject.Delete, IGroupPolicyObject::Delete, _win32_igrouppolicyobject_delete, gpedit/IGroupPolicyObject::Delete, policy.igrouppolicyobject_delete
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
 - IGroupPolicyObject::Delete
 - gpedit/IGroupPolicyObject::Delete
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
 - IGroupPolicyObject.Delete
---

# IGroupPolicyObject::Delete


## -description

The
    <b>Delete</b> method deletes the GPO.



## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

After calling this method, you cannot call other methods of the 
<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a> interface because all data has been deleted for the GPO.

<div class="alert"><b>Note</b>  A policy refresh will not automatically be triggered when the local Group Policy object is deleted using the <b>Delete</b> method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-save">Save</a>
