---
UID: NF:comadmin.ICOMAdminCatalog2.ImportUnconfiguredComponents
title: ICOMAdminCatalog2::ImportUnconfiguredComponents (comadmin.h)
description: Imports the specified classes into a COM+ application as unconfigured components.
helpviewer_keywords: ["COMAdmin32BitComponent","COMAdmin64BitComponent","ICOMAdminCatalog2 interface [COM+]","ImportUnconfiguredComponents method","ICOMAdminCatalog2.ImportUnconfiguredComponents","ICOMAdminCatalog2::ImportUnconfiguredComponents","ImportUnconfiguredComponents","ImportUnconfiguredComponents method [COM+]","ImportUnconfiguredComponents method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_ImportUnconfiguredComponents","comadmin/ICOMAdminCatalog2::ImportUnconfiguredComponents","cos.icomadmincatalog2_importunconfiguredcomponents"]
old-location: cos\icomadmincatalog2_importunconfiguredcomponents.htm
tech.root: cos
ms.assetid: 51bab6c7-5ec2-4651-a0c4-c54683a65d75
ms.date: 12/05/2018
ms.keywords: COMAdmin32BitComponent, COMAdmin64BitComponent, ICOMAdminCatalog2 interface [COM+],ImportUnconfiguredComponents method, ICOMAdminCatalog2.ImportUnconfiguredComponents, ICOMAdminCatalog2::ImportUnconfiguredComponents, ImportUnconfiguredComponents, ImportUnconfiguredComponents method [COM+], ImportUnconfiguredComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_ImportUnconfiguredComponents, comadmin/ICOMAdminCatalog2::ImportUnconfiguredComponents, cos.icomadmincatalog2_importunconfiguredcomponents
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
 - ICOMAdminCatalog2::ImportUnconfiguredComponents
 - comadmin/ICOMAdminCatalog2::ImportUnconfiguredComponents
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
 - ICOMAdminCatalog2.ImportUnconfiguredComponents
---

# ICOMAdminCatalog2::ImportUnconfiguredComponents


## -description

Imports the specified classes into a COM+ application as unconfigured components.

## -parameters

### -param bstrApplicationIDOrName [in]

The application ID or name of the application into which the components are to be imported.

### -param pVarCLSIDOrProgID [in]

The unconfigured components to be imported. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

### -param pVarComponentType [in, optional]

The bitnes of each component. This parameter can be one of the following values. If this parameter is omitted, the native bitness of the computer is assumed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdmin32BitComponent"></a><a id="comadmin32bitcomponent"></a><a id="COMADMIN32BITCOMPONENT"></a><dl>
<dt><b>COMAdmin32BitComponent</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Uses a 32-bit format.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdmin64BitComponent"></a><a id="comadmin64bitcomponent"></a><a id="COMADMIN64BITCOMPONENT"></a><dl>
<dt><b>COMAdmin64BitComponent</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Uses a 64-bit format.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog2">ICOMAdminCatalog2</a>