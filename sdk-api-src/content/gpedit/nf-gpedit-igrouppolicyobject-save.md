---
UID: NF:gpedit.IGroupPolicyObject.Save
title: IGroupPolicyObject::Save
author: windows-sdk-content
description: The Save method saves the specified registry policy settings to disk and updates the revision number of the GPO.
old-location: policy\igrouppolicyobject_save.htm
old-project: policy
ms.assetid: e3713e5f-c710-48f7-8081-f2669c77449d
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IGroupPolicyObject interface [Group Policy],Save method, IGroupPolicyObject.Save, IGroupPolicyObject::Save, Save, Save method [Group Policy], Save method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_save, gpedit/IGroupPolicyObject::Save, policy.igrouppolicyobject_save
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.Save
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/34afb04e-47f9-4d7c-9fa6-9d76188d7e05">Delete</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/e251cac2-8fc8-4ed0-b940-4a9f47eca26b">New</a>
 

 

