---
UID: NF:comadmin.ICOMAdminCatalog2.AliasComponent
title: ICOMAdminCatalog2::AliasComponent (comadmin.h)
description: Creates an alias for an existing COM+ component.
helpviewer_keywords: ["AliasComponent","AliasComponent method [COM+]","AliasComponent method [COM+]","ICOMAdminCatalog2 interface","ICOMAdminCatalog2 interface [COM+]","AliasComponent method","ICOMAdminCatalog2.AliasComponent","ICOMAdminCatalog2::AliasComponent","_cos_icomadmincatalog2_AliasComponent","comadmin/ICOMAdminCatalog2::AliasComponent","cos.icomadmincatalog2_aliascomponent"]
old-location: cos\icomadmincatalog2_aliascomponent.htm
tech.root: cos
ms.assetid: 99d43ef5-f117-4307-aa44-f149b4986cda
ms.date: 12/05/2018
ms.keywords: AliasComponent, AliasComponent method [COM+], AliasComponent method [COM+],ICOMAdminCatalog2 interface, ICOMAdminCatalog2 interface [COM+],AliasComponent method, ICOMAdminCatalog2.AliasComponent, ICOMAdminCatalog2::AliasComponent, _cos_icomadmincatalog2_AliasComponent, comadmin/ICOMAdminCatalog2::AliasComponent, cos.icomadmincatalog2_aliascomponent
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
 - ICOMAdminCatalog2::AliasComponent
 - comadmin/ICOMAdminCatalog2::AliasComponent
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
 - ICOMAdminCatalog2.AliasComponent
---

# ICOMAdminCatalog2::AliasComponent


## -description

Creates an alias for an existing COM+ component.

## -parameters

### -param bstrSrcApplicationIDOrName [in]

The application ID or name of the source application containing the component.

### -param bstrCLSIDOrProgID [in]

The class ID or program ID of the component for which an alias is created.

### -param bstrDestApplicationIDOrName [in]

The application ID or the name of the destination application that contains the alias. If this argument is <b>NULL</b> or an empty string, the alias is created within the source application.

### -param bstrNewProgId [in]

The program ID of the alias.

### -param bstrNewClsid [in]

The class ID of the alias. If this argument is <b>NULL</b> or an empty string, a new, unique class ID is assigned.

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
<dt><b>COMADMIN_E_AMBIGUOUS_APPLICATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
At least one of the named applications exists in multiple partitions. To avoid this error, use application IDs instead of names.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>