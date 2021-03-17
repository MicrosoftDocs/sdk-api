---
UID: NF:comadmin.ICOMAdminCatalog2.AreApplicationInstancesPaused
title: ICOMAdminCatalog2::AreApplicationInstancesPaused (comadmin.h)
description: Determines whether any of the specified application instances (processes) are paused.
helpviewer_keywords: ["AreApplicationInstancesPaused","AreApplicationInstancesPaused method [COM+]","AreApplicationInstancesPaused method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","AreApplicationInstancesPaused method","ICOMAdminCatalog2.AreApplicationInstancesPaused","ICOMAdminCatalog2::AreApplicationInstancesPaused","_cos_icomadmincatalog2_AreApplicationInstancesPaused","comadmin/ICOMAdminCatalog2::AreApplicationInstancesPaused","cos.icomadmincatalog2_areapplicationinstancespaused"]
old-location: cos\icomadmincatalog2_areapplicationinstancespaused.htm
tech.root: cos
ms.assetid: b526dc2e-107c-4936-95ac-2c0c91f5c09b
ms.date: 12/05/2018
ms.keywords: AreApplicationInstancesPaused, AreApplicationInstancesPaused method [COM+], AreApplicationInstancesPaused method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],AreApplicationInstancesPaused method, ICOMAdminCatalog2.AreApplicationInstancesPaused, ICOMAdminCatalog2::AreApplicationInstancesPaused, _cos_icomadmincatalog2_AreApplicationInstancesPaused, comadmin/ICOMAdminCatalog2::AreApplicationInstancesPaused, cos.icomadmincatalog2_areapplicationinstancespaused
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog2::AreApplicationInstancesPaused
 - comadmin/ICOMAdminCatalog2::AreApplicationInstancesPaused
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2.AreApplicationInstancesPaused
---

# ICOMAdminCatalog2::AreApplicationInstancesPaused


## -description

Determines whether any of the specified application instances (processes) are paused.

## -parameters

### -param pVarApplicationInstanceID [in]

The application instances to be checked. Each element of the <b>Variant</b> may be a <b>String</b> containing an application instance ID (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getapplicationinstanceidfromprocessid">GetApplicationInstanceIDFromProcessID</a> method), a single catalog object, or a catalog collection (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

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

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>