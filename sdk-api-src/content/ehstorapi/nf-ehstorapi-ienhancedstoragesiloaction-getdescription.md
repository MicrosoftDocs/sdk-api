---
UID: NF:ehstorapi.IEnhancedStorageSiloAction.GetDescription
title: IEnhancedStorageSiloAction::GetDescription (ehstorapi.h)
description: Returns a descriptive string for the action specified by the IEnhancedStorageSiloAction object.
helpviewer_keywords: ["GetDescription","GetDescription method [Enhanced Storage]","GetDescription method [Enhanced Storage]","IEnhancedStorageSiloAction interface","IEnhancedStorageSiloAction interface [Enhanced Storage]","GetDescription method","IEnhancedStorageSiloAction.GetDescription","IEnhancedStorageSiloAction::GetDescription","ehstorapi/IEnhancedStorageSiloAction::GetDescription","enstor.ienhancedstoragesiloaction_getdescription"]
old-location: enstor\ienhancedstoragesiloaction_getdescription.htm
tech.root: enstor
ms.assetid: 1eb94182-520e-40a6-87e6-6ead2ab2e188
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Enhanced Storage], GetDescription method [Enhanced Storage],IEnhancedStorageSiloAction interface, IEnhancedStorageSiloAction interface [Enhanced Storage],GetDescription method, IEnhancedStorageSiloAction.GetDescription, IEnhancedStorageSiloAction::GetDescription, ehstorapi/IEnhancedStorageSiloAction::GetDescription, enstor.ienhancedstoragesiloaction_getdescription
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
 - IEnhancedStorageSiloAction::GetDescription
 - ehstorapi/IEnhancedStorageSiloAction::GetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageSiloAction.GetDescription
---

# IEnhancedStorageSiloAction::GetDescription


## -description

Returns a descriptive string for the action specified by the <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageSiloAction</a> object.

## -parameters

### -param ppwszActionDescription [out]

Pointer to a string that describes the silo action.

## -returns

This method can return one of these values.

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
The descriptive string was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppwszDescription</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The description string is brief, consisting of one or two short sentences, and is suitable for display in a UI element such as tooltip or small static text box.

When the caller no longer requires access to the string, this buffer must be freed by passing this pointer to <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageSiloAction</a>