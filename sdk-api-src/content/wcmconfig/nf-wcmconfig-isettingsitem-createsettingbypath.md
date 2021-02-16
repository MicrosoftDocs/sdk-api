---
UID: NF:wcmconfig.ISettingsItem.CreateSettingByPath
title: ISettingsItem::CreateSettingByPath (wcmconfig.h)
description: Creates a setting object specified by the path.
helpviewer_keywords: ["CreateSettingByPath","CreateSettingByPath method [SMI]","CreateSettingByPath method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","CreateSettingByPath method","ISettingsItem.CreateSettingByPath","ISettingsItem::CreateSettingByPath","smi.isettingsitem_createsettingbypath","wcmconfig/ISettingsItem::CreateSettingByPath"]
old-location: smi\isettingsitem_createsettingbypath.htm
tech.root: SMI
ms.assetid: 8b51329e-dc81-46dc-b174-0191e2eea44a
ms.date: 12/05/2018
ms.keywords: CreateSettingByPath, CreateSettingByPath method [SMI], CreateSettingByPath method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],CreateSettingByPath method, ISettingsItem.CreateSettingByPath, ISettingsItem::CreateSettingByPath, smi.isettingsitem_createsettingbypath, wcmconfig/ISettingsItem::CreateSettingByPath
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
 - ISettingsItem::CreateSettingByPath
 - wcmconfig/ISettingsItem::CreateSettingByPath
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
 - ISettingsItem.CreateSettingByPath
---

# ISettingsItem::CreateSettingByPath


## -description

Creates a setting object specified by the path.

## -parameters

### -param Path [in]

A pointer to the path.

### -param Setting [out]

A pointer to the newly created <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> item.

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
<dt><b>WCM_E_STATENODENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is called to create an item that is not a list element or does not already exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, such as if it is a read only item, or the namespace was opened in ReadOnly mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDVALUE, WCM_E_INVALIDVALUEFORMAT, or WCM_E_INVALIDDATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the value provided for the key cannot be coerced to the appropriate type, such as a string value coerced to an unsigned integer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_WRONGESCAPESTRING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path contains an unrecognized XML escape sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDKEY</b></dt>
</dl>
</td>
<td width="60%">
 Indicates that the path is incorrectly specified and references the wrong key for a list item.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  When creating a scalar list item, you must set a value on the resulting <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> before releasing it, or it will not be persisted.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>