---
UID: NF:comadmin.ICOMAdminCatalog2.RecycleApplicationInstances
title: ICOMAdminCatalog2::RecycleApplicationInstances (comadmin.h)
description: Recycles (shuts down and restarts) the specified application server processes.helpviewer_keywords: ["ICOMAdminCatalog2 interface [COM+]","RecycleApplicationInstances method","ICOMAdminCatalog2.RecycleApplicationInstances","ICOMAdminCatalog2::RecycleApplicationInstances","RecycleApplicationInstances","RecycleApplicationInstances method [COM+]","RecycleApplicationInstances method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_RecycleApplicationInstances","comadmin/ICOMAdminCatalog2::RecycleApplicationInstances","cos.icomadmincatalog2_recycleapplicationinstances"]
old-location: cos\icomadmincatalog2_recycleapplicationinstances.htm
tech.root: cossdk
ms.assetid: 0d2d6255-54c7-4110-9ee0-7019e9c7cb83
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],RecycleApplicationInstances method, ICOMAdminCatalog2.RecycleApplicationInstances, ICOMAdminCatalog2::RecycleApplicationInstances, RecycleApplicationInstances, RecycleApplicationInstances method [COM+], RecycleApplicationInstances method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_RecycleApplicationInstances, comadmin/ICOMAdminCatalog2::RecycleApplicationInstances, cos.icomadmincatalog2_recycleapplicationinstances
f1_keywords:
- comadmin/ICOMAdminCatalog2.RecycleApplicationInstances
dev_langs:
- c++
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComAdmin.h
api_name:
- ICOMAdminCatalog2.RecycleApplicationInstances
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog2::RecycleApplicationInstances


## -description


Recycles (shuts down and restarts) the specified application server processes.


## -parameters




### -param pVarApplicationInstanceID [in]

The application instances to be recycled. Each element of the <b>Variant</b> may be a <b>String</b> containing an application instance GUID (for example, as returned by the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getapplicationinstanceidfromprocessid">GetApplicationInstanceIDFromProcessID</a> method), a single catalog object, or a catalog collection (for example, as returned by the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).


### -param lReasonCode [in]

The reason for recycling the specified application instances. This code is written to an event log entry.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADIN_E_OBJECT_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
A specified application instance does not exist.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>
 

 

