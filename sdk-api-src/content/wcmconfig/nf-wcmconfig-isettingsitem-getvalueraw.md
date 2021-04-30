---
UID: NF:wcmconfig.ISettingsItem.GetValueRaw
title: ISettingsItem::GetValueRaw (wcmconfig.h)
description: Gets the value from the current item as a byte array.
helpviewer_keywords: ["GetValueRaw","GetValueRaw method [SMI]","GetValueRaw method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetValueRaw method","ISettingsItem.GetValueRaw","ISettingsItem::GetValueRaw","smi.isettingsitem_getvalueraw","wcmconfig/ISettingsItem::GetValueRaw"]
old-location: smi\isettingsitem_getvalueraw.htm
tech.root: SMI
ms.assetid: 2b4b96df-1286-49be-869a-404adaead27a
ms.date: 12/05/2018
ms.keywords: GetValueRaw, GetValueRaw method [SMI], GetValueRaw method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetValueRaw method, ISettingsItem.GetValueRaw, ISettingsItem::GetValueRaw, smi.isettingsitem_getvalueraw, wcmconfig/ISettingsItem::GetValueRaw
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISettingsItem::GetValueRaw
 - wcmconfig/ISettingsItem::GetValueRaw
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsItem.GetValueRaw
---

# ISettingsItem::GetValueRaw


## -description

Gets the value from the current item as
    a byte array.
<div class="alert"><b>Note</b>  The caller must release the
    returned byte array by calling CoTaskMemFree.</div><div> </div>

## -parameters

### -param Data [out]

An array of BYTE pointers, allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, of length DataSize.

### -param DataSize [out]

The length of the data.

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
Indicates success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item is not a scalar setting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY </b></dt>
</dl>
</td>
<td width="60%">
Indicates that there are insufficient resources to allocate the return data. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there is no value for the item.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>