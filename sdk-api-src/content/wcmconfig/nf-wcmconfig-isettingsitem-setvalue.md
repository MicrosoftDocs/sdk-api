---
UID: NF:wcmconfig.ISettingsItem.SetValue
title: ISettingsItem::SetValue (wcmconfig.h)
description: Sets the value of an item.
helpviewer_keywords: ["ISettingsItem interface [SMI]","SetValue method","ISettingsItem.SetValue","ISettingsItem::SetValue","SetValue","SetValue method [SMI]","SetValue method [SMI]","ISettingsItem interface","smi.isettingsitem_setvalue","wcmconfig/ISettingsItem::SetValue"]
old-location: smi\isettingsitem_setvalue.htm
tech.root: SMI
ms.assetid: 52b7e852-b389-47ec-a9d0-e4ce2e95f1f8
ms.date: 12/05/2018
ms.keywords: ISettingsItem interface [SMI],SetValue method, ISettingsItem.SetValue, ISettingsItem::SetValue, SetValue, SetValue method [SMI], SetValue method [SMI],ISettingsItem interface, smi.isettingsitem_setvalue, wcmconfig/ISettingsItem::SetValue
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
 - ISettingsItem::SetValue
 - wcmconfig/ISettingsItem::SetValue
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
 - ISettingsItem.SetValue
---

# ISettingsItem::SetValue


## -description

Sets the value of an item.

## -parameters

### -param Value [in]

Variant that contains the value of the item.

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