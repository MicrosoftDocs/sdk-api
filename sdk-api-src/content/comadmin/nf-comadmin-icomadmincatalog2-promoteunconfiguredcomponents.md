---
UID: NF:comadmin.ICOMAdminCatalog2.PromoteUnconfiguredComponents
title: ICOMAdminCatalog2::PromoteUnconfiguredComponents (comadmin.h)
description: Promotes the specified classes from unconfigured components to configured components.
helpviewer_keywords: ["COMAdmin32BitComponent","COMAdmin64BitComponent","ICOMAdminCatalog2 interface [COM+]","PromoteUnconfiguredComponents method","ICOMAdminCatalog2.PromoteUnconfiguredComponents","ICOMAdminCatalog2::PromoteUnconfiguredComponents","PromoteUnconfiguredComponents","PromoteUnconfiguredComponents method [COM+]","PromoteUnconfiguredComponents method [COM+]","ICOMAdminCatalog2 interface","_cos_icomadmincatalog2_PromoteUnconfiguredComponents","comadmin/ICOMAdminCatalog2::PromoteUnconfiguredComponents","cos.icomadmincatalog2_promoteunconfiguredcomponents"]
old-location: cos\icomadmincatalog2_promoteunconfiguredcomponents.htm
tech.root: cos
ms.assetid: e6ed7fa7-3736-4e82-a153-116f4aa141a1
ms.date: 12/05/2018
ms.keywords: COMAdmin32BitComponent, COMAdmin64BitComponent, ICOMAdminCatalog2 interface [COM+],PromoteUnconfiguredComponents method, ICOMAdminCatalog2.PromoteUnconfiguredComponents, ICOMAdminCatalog2::PromoteUnconfiguredComponents, PromoteUnconfiguredComponents, PromoteUnconfiguredComponents method [COM+], PromoteUnconfiguredComponents method [COM+],ICOMAdminCatalog2 interface, _cos_icomadmincatalog2_PromoteUnconfiguredComponents, comadmin/ICOMAdminCatalog2::PromoteUnconfiguredComponents, cos.icomadmincatalog2_promoteunconfiguredcomponents
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
 - ICOMAdminCatalog2::PromoteUnconfiguredComponents
 - comadmin/ICOMAdminCatalog2::PromoteUnconfiguredComponents
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
 - ICOMAdminCatalog2.PromoteUnconfiguredComponents
---

# ICOMAdminCatalog2::PromoteUnconfiguredComponents


## -description

Promotes the specified classes from unconfigured components to configured components.
<div class="alert"><b>Note</b>  Before calling this method, its necessary to first import the unconfigured components by using the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-importunconfiguredcomponents">ImportUnconfiguredComponents</a> method. Otherwise, this method returns an E_INVALIDARG error.</div><div> </div>

## -parameters

### -param bstrApplicationIDOrName [in]

The application ID or name of the application containing the components to be promoted.

### -param pVarCLSIDOrProgID [in]

The unconfigured components to be promoted. Each element of the <b>Variant</b> may be a <b>String</b> containing a class ID or program ID, a single catalog object, or a catalog collection (for example, as returned by the <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a> method).

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