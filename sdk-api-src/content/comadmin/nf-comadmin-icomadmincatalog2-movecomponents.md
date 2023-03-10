---
UID: NF:comadmin.ICOMAdminCatalog2.MoveComponents
title: ICOMAdminCatalog2::MoveComponents (comadmin.h)
description: Moves the specified components from one application to another.
helpviewer_keywords: ["ICOMAdminCatalog2 interface [COM+]","MoveComponents method","ICOMAdminCatalog2.MoveComponents","ICOMAdminCatalog2::MoveComponents","MoveComponents","MoveComponents method [COM+]","MoveComponents method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_MoveComponents","comadmin/ICOMAdminCatalog2::MoveComponents","cos.icomadmincatalog2_movecomponents"]
old-location: cos\icomadmincatalog2_movecomponents.htm
tech.root: cos
ms.assetid: 38cc4726-4b61-4f4b-9719-161297361f45
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog2 interface [COM+],MoveComponents method, ICOMAdminCatalog2.MoveComponents, ICOMAdminCatalog2::MoveComponents, MoveComponents, MoveComponents method [COM+], MoveComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_MoveComponents, comadmin/ICOMAdminCatalog2::MoveComponents, cos.icomadmincatalog2_movecomponents
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
 - ICOMAdminCatalog2::MoveComponents
 - comadmin/ICOMAdminCatalog2::MoveComponents
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
 - ICOMAdminCatalog2.MoveComponents
---

# ICOMAdminCatalog2::MoveComponents


## -description

Moves the specified components from one application to another.

## -parameters

### -param bstrSourceApplicationIDOrName [in]

The application ID or name of the source application.

### -param pVarCLSIDOrProgID [in]

The components to be moved. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

### -param bstrDestinationApplicationIDOrName [in]

The application ID or name of the destination application.

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
<dt><b>COMADIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
At least one of the named applications exists in multiple partitions. To avoid this error, use application IDs instead of names.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>