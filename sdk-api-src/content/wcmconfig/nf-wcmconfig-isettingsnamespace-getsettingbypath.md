---
UID: NF:wcmconfig.ISettingsNamespace.GetSettingByPath
title: ISettingsNamespace::GetSettingByPath (wcmconfig.h)
description: Gets the setting object specified by a path.
helpviewer_keywords: ["GetSettingByPath","GetSettingByPath method [SMI]","GetSettingByPath method [SMI]","ISettingsNamespace interface","ISettingsNamespace interface [SMI]","GetSettingByPath method","ISettingsNamespace.GetSettingByPath","ISettingsNamespace::GetSettingByPath","smi.isettingsnamespace_getsettingbypath","wcmconfig/ISettingsNamespace::GetSettingByPath"]
old-location: smi\isettingsnamespace_getsettingbypath.htm
tech.root: SMI
ms.assetid: 7deadfed-036d-40cd-88b6-7afaf8fc7d41
ms.date: 12/05/2018
ms.keywords: GetSettingByPath, GetSettingByPath method [SMI], GetSettingByPath method [SMI],ISettingsNamespace interface, ISettingsNamespace interface [SMI],GetSettingByPath method, ISettingsNamespace.GetSettingByPath, ISettingsNamespace::GetSettingByPath, smi.isettingsnamespace_getsettingbypath, wcmconfig/ISettingsNamespace::GetSettingByPath
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
 - ISettingsNamespace::GetSettingByPath
 - wcmconfig/ISettingsNamespace::GetSettingByPath
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
 - ISettingsNamespace.GetSettingByPath
---

# ISettingsNamespace::GetSettingByPath


## -description

Gets the setting object specified by a path.

## -parameters

### -param Path [in]

The path of the object.

### -param Setting [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> object that represents the retrieved object.

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
<dt><b>WCM_E_INVALIDPATH</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path is not formatted correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDKEY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path contains an unrecognized XML escape sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_WRONGESCAPESTRING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the path is incorrectly specified and references the wrong key for a list item.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a>