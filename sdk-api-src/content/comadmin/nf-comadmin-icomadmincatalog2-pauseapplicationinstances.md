---
UID: NF:comadmin.ICOMAdminCatalog2.PauseApplicationInstances
title: ICOMAdminCatalog2::PauseApplicationInstances (comadmin.h)
description: Pauses the specified application server processes.
helpviewer_keywords: ["ICOMAdminCatalog2 interface [COM+]","PauseApplicationInstances method","ICOMAdminCatalog2.PauseApplicationInstances","ICOMAdminCatalog2::PauseApplicationInstances","PauseApplicationInstances","PauseApplicationInstances method [COM+]","PauseApplicationInstances method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_PauseApplicationInstances","comadmin/ICOMAdminCatalog2::PauseApplicationInstances","cos.icomadmincatalog2_pauseapplicationinstances"]
old-location: cos\icomadmincatalog2_pauseapplicationinstances.htm
tech.root: cos
ms.assetid: 59771a5d-894b-46de-9874-ece4aca7232f
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],PauseApplicationInstances method, ICOMAdminCatalog2.PauseApplicationInstances, ICOMAdminCatalog2::PauseApplicationInstances, PauseApplicationInstances, PauseApplicationInstances method [COM+], PauseApplicationInstances method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_PauseApplicationInstances, comadmin/ICOMAdminCatalog2::PauseApplicationInstances, cos.icomadmincatalog2_pauseapplicationinstances
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
 - ICOMAdminCatalog2::PauseApplicationInstances
 - comadmin/ICOMAdminCatalog2::PauseApplicationInstances
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
 - ICOMAdminCatalog2.PauseApplicationInstances
---

# ICOMAdminCatalog2::PauseApplicationInstances


## -description

Pauses the specified application server processes.

## -parameters

### -param pVarApplicationInstanceID [in]

The application instances to be paused. Each element of the <b>Variant</b> may be a <b>String</b> containing an application instance GUID (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getapplicationinstanceidfromprocessid">GetApplicationInstanceIDFromProcessID</a> method), a single catalog object, or a catalog collection (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

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