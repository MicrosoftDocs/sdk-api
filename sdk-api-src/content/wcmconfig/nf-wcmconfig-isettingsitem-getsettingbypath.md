---
UID: NF:wcmconfig.ISettingsItem.GetSettingByPath
title: ISettingsItem::GetSettingByPath (wcmconfig.h)
description: Gets a setting based on the given path.
helpviewer_keywords: ["GetSettingByPath","GetSettingByPath method [SMI]","GetSettingByPath method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetSettingByPath method","ISettingsItem.GetSettingByPath","ISettingsItem::GetSettingByPath","smi.isettingsitem_getsettingbypath","wcmconfig/ISettingsItem::GetSettingByPath"]
old-location: smi\isettingsitem_getsettingbypath.htm
tech.root: SMI
ms.assetid: a4270c46-b214-4232-b414-d6b6e4e35635
ms.date: 12/05/2018
ms.keywords: GetSettingByPath, GetSettingByPath method [SMI], GetSettingByPath method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetSettingByPath method, ISettingsItem.GetSettingByPath, ISettingsItem::GetSettingByPath, smi.isettingsitem_getsettingbypath, wcmconfig/ISettingsItem::GetSettingByPath
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
 - ISettingsItem::GetSettingByPath
 - wcmconfig/ISettingsItem::GetSettingByPath
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
 - ISettingsItem.GetSettingByPath
---

# ISettingsItem::GetSettingByPath


## -description

Gets a setting based on the given path.

## -parameters

### -param Path [in]

Path of the list element or attribute to retrieve. The path is relative to the current setting.

### -param Setting [out]

 An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> interface pointer used to access the item.

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
Indicates an attempt to get an item that does not exist.

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
<dt><b>WCM_E_INVALIDPATH</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path is incorrectly formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDKEY </b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path is incorrectly specified and references the wrong key for the list item.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>