---
UID: NF:comadmin.ICOMAdminCatalog2.AreApplicationInstancesPaused
title: ICOMAdminCatalog2::AreApplicationInstancesPaused
author: windows-driver-content
description: Determines whether any of the specified application instances (processes) are paused.
old-location: cos\icomadmincatalog2_areapplicationinstancespaused.htm
old-project: cossdk
ms.assetid: b526dc2e-107c-4936-95ac-2c0c91f5c09b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: AreApplicationInstancesPaused, AreApplicationInstancesPaused method [COM+], AreApplicationInstancesPaused method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],AreApplicationInstancesPaused method, ICOMAdminCatalog2.AreApplicationInstancesPaused, ICOMAdminCatalog2::AreApplicationInstancesPaused, _cos_icomadmincatalog2_AreApplicationInstancesPaused, comadmin/ICOMAdminCatalog2::AreApplicationInstancesPaused, cos.icomadmincatalog2_areapplicationinstancespaused
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog2.AreApplicationInstancesPaused
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2::AreApplicationInstancesPaused


## -description


Determines whether any of the specified application instances (processes) are paused.


## -parameters




### -param pVarApplicationInstanceID [in]

The application instances to be checked. Each element of the <b>Variant</b> may be a <b>String</b> containing an application instance ID (for example, as returned by the <a href="https://msdn.microsoft.com/a09569af-11ec-406a-a51c-72b81b84fe41">GetApplicationInstanceIDFromProcessID</a> method), a single catalog object, or a catalog collection (for example, as returned by the <a href="https://msdn.microsoft.com/b1861e8f-bb42-42b5-9435-6fa366f8284a">GetCollectionByQuery2</a> method).


### -param pVarBoolPaused [out, retval]

Indicates whether the specified applications are paused.


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




<a href="https://msdn.microsoft.com/ffca611d-dacc-47be-9101-9de76ecc8393">ICOMAdminCatalog2</a>
 

 

