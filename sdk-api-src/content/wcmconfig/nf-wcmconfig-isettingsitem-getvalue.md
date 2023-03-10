---
UID: NF:wcmconfig.ISettingsItem.GetValue
title: ISettingsItem::GetValue (wcmconfig.h)
description: Gets the current value from the item.
helpviewer_keywords: ["GetValue","GetValue method [SMI]","GetValue method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetValue method","ISettingsItem.GetValue","ISettingsItem::GetValue","smi.isettingsitem_getvalue","wcmconfig/ISettingsItem::GetValue"]
old-location: smi\isettingsitem_getvalue.htm
tech.root: SMI
ms.assetid: 11b61570-d1ed-4dcf-b533-873096ae80b9
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [SMI], GetValue method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetValue method, ISettingsItem.GetValue, ISettingsItem::GetValue, smi.isettingsitem_getvalue, wcmconfig/ISettingsItem::GetValue
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
 - ISettingsItem::GetValue
 - wcmconfig/ISettingsItem::GetValue
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
 - ISettingsItem.GetValue
---

# ISettingsItem::GetValue


## -description

Gets the current value from the item.

## -parameters

### -param Value [out]

The value of the item.

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