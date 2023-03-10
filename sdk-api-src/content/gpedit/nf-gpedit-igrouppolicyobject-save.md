---
UID: NF:gpedit.IGroupPolicyObject.Save
title: IGroupPolicyObject::Save (gpedit.h)
description: The Save method saves the specified registry policy settings to disk and updates the revision number of the GPO.
helpviewer_keywords: ["IGroupPolicyObject interface [Group Policy]","Save method","IGroupPolicyObject.Save","IGroupPolicyObject::Save","Save","Save method [Group Policy]","Save method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_save","gpedit/IGroupPolicyObject::Save","policy.igrouppolicyobject_save"]
old-location: policy\igrouppolicyobject_save.htm
tech.root: Policy
ms.assetid: e3713e5f-c710-48f7-8081-f2669c77449d
ms.date: 12/05/2018
ms.keywords: IGroupPolicyObject interface [Group Policy],Save method, IGroupPolicyObject.Save, IGroupPolicyObject::Save, Save, Save method [Group Policy], Save method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_save, gpedit/IGroupPolicyObject::Save, policy.igrouppolicyobject_save
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
 - IGroupPolicyObject::Save
 - gpedit/IGroupPolicyObject::Save
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
 - IGroupPolicyObject.Save
---

# IGroupPolicyObject::Save


## -description

The
    <b>Save</b> method saves the specified registry policy settings to disk and updates the revision number of the GPO.

## -parameters

### -param bMachine [in]

Specifies the registry policy settings to be saved. If this parameter is <b>TRUE</b>, the computer policy settings are saved. Otherwise, the user policy settings are saved.

### -param bAdd [in]

Specifies whether this is an add or delete operation. If this parameter is <b>FALSE</b>,  the last policy setting for the specified extension <i>pGuidExtension</i> is removed. In all other cases, this parameter is <b>TRUE</b>.

### -param pGuidExtension [in]

Specifies the GUID or unique name of the snap-in extension that will process policy. If the GPO is to be processed by the snap-in that processes .pol files, you must specify the REGISTRY_EXTENSION_GUID value.

### -param pGuid [in]

Specifies the GUID that identifies the MMC snap-in used to edit this policy. The snap-in can be a Microsoft snap-in or a third-party snap-in.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

<div class="alert"><b>Note</b>  A policy refresh will be automatically triggered when the user or computer portion of the local Group Policy object is enabled or disabled using the  <b>Save</b> method.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-delete">Delete</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-new">New</a>