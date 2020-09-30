---
UID: NF:comadmin.ICOMAdminCatalog.InstallMultipleComponents
title: ICOMAdminCatalog::InstallMultipleComponents (comadmin.h)
description: Installs components from multiple files into a COM+ application.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","InstallMultipleComponents method","ICOMAdminCatalog.InstallMultipleComponents","ICOMAdminCatalog::InstallMultipleComponents","InstallMultipleComponents","InstallMultipleComponents method [COM+]","InstallMultipleComponents method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_InstallMultipleComponents","comadmin/ICOMAdminCatalog::InstallMultipleComponents","cos.icomadmincatalog_installmultiplecomponents"]
old-location: cos\icomadmincatalog_installmultiplecomponents.htm
tech.root: cos
ms.assetid: 7206c93b-43ca-402f-9a55-930f872d4201
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],InstallMultipleComponents method, ICOMAdminCatalog.InstallMultipleComponents, ICOMAdminCatalog::InstallMultipleComponents, InstallMultipleComponents, InstallMultipleComponents method [COM+], InstallMultipleComponents method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_InstallMultipleComponents, comadmin/ICOMAdminCatalog::InstallMultipleComponents, cos.icomadmincatalog_installmultiplecomponents
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ICOMAdminCatalog::InstallMultipleComponents
 - comadmin/ICOMAdminCatalog::InstallMultipleComponents
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
 - ICOMAdminCatalog.InstallMultipleComponents
---

# ICOMAdminCatalog::InstallMultipleComponents


## -description

Installs components from multiple files into a COM+ application.

## -parameters

### -param bstrApplIDOrName [in]

The GUID or name of the application.

### -param ppsaVarFileNames [in]

An array of the names of the DLL files that contains the components to be installed.

### -param ppsaVarCLSIDs [in]

An array of CLSIDs for the components to be installed.

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
<dt><b>COMADMIN_E_OBJECTERRORS</b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>