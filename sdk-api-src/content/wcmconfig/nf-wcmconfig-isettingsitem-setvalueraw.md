---
UID: NF:wcmconfig.ISettingsItem.SetValueRaw
title: ISettingsItem::SetValueRaw (wcmconfig.h)
description: Sets the value of the current item by supplying data in raw form.
helpviewer_keywords: ["ISettingsItem interface [SMI]","SetValueRaw method","ISettingsItem.SetValueRaw","ISettingsItem::SetValueRaw","SetValueRaw","SetValueRaw method [SMI]","SetValueRaw method [SMI]","ISettingsItem interface","smi.isettingsitem_setvalueraw","wcmconfig/ISettingsItem::SetValueRaw"]
old-location: smi\isettingsitem_setvalueraw.htm
tech.root: SMI
ms.assetid: 65925c16-7a12-440f-ba2d-9156e41049ba
ms.date: 12/05/2018
ms.keywords: ISettingsItem interface [SMI],SetValueRaw method, ISettingsItem.SetValueRaw, ISettingsItem::SetValueRaw, SetValueRaw, SetValueRaw method [SMI], SetValueRaw method [SMI],ISettingsItem interface, smi.isettingsitem_setvalueraw, wcmconfig/ISettingsItem::SetValueRaw
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
 - ISettingsItem::SetValueRaw
 - wcmconfig/ISettingsItem::SetValueRaw
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
 - ISettingsItem.SetValueRaw
---

# ISettingsItem::SetValueRaw


## -description

Sets the value of the current item by supplying data in raw form.

## -parameters

### -param DataType [in]

The data type of the item.

### -param Data [in]

A byte array that contains the value of the item.

### -param DataSize [in]

The size of the byte array.

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
<dt><b>WCM_E_INVALIDVALUE, WCM_E_INVALIDVALUEFORMAT, or WCM_E_INVALIDDATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the value is not of the correct type for the item, or that the value cannot be coerced to the correct type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, either because it is a read-only item, or because the namespace was opened in ReadOnly mode.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>