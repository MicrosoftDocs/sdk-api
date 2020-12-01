---
UID: NF:ehstorapi.IEnhancedStorageSiloAction.GetName
title: IEnhancedStorageSiloAction::GetName (ehstorapi.h)
description: Returns a string for the name of the action specified by the IEnhancedStorageSiloAction object.
helpviewer_keywords: ["GetName","GetName method [Enhanced Storage]","GetName method [Enhanced Storage]","IEnhancedStorageSiloAction interface","IEnhancedStorageSiloAction interface [Enhanced Storage]","GetName method","IEnhancedStorageSiloAction.GetName","IEnhancedStorageSiloAction::GetName","ehstorapi/IEnhancedStorageSiloAction::GetName","enstor.ienhancedstoragesiloaction_getname"]
old-location: enstor\ienhancedstoragesiloaction_getname.htm
tech.root: enstor
ms.assetid: 3690d395-c83e-4253-adc2-d30a96a5ce47
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Enhanced Storage], GetName method [Enhanced Storage],IEnhancedStorageSiloAction interface, IEnhancedStorageSiloAction interface [Enhanced Storage],GetName method, IEnhancedStorageSiloAction.GetName, IEnhancedStorageSiloAction::GetName, ehstorapi/IEnhancedStorageSiloAction::GetName, enstor.ienhancedstoragesiloaction_getname
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
 - IEnhancedStorageSiloAction::GetName
 - ehstorapi/IEnhancedStorageSiloAction::GetName
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
 - IEnhancedStorageSiloAction.GetName
---

# IEnhancedStorageSiloAction::GetName


## -description

Returns a string for the name of the action specified by the <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageSiloAction</a> object.

## -parameters

### -param ppwszActionName [out]

Pointer to a string that represents the silo action by name.

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
The  action name was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppwszActionName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A name string is short, consisting of one or two words, and is suitable for display in a UI element such as a menu item or button label.

When the caller no longer requires access to the string, this buffer must be freed by passing this pointer to <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageSiloAction</a>