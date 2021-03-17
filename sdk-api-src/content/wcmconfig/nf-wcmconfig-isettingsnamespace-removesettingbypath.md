---
UID: NF:wcmconfig.ISettingsNamespace.RemoveSettingByPath
title: ISettingsNamespace::RemoveSettingByPath (wcmconfig.h)
description: Removes the setting object specified by a path.
helpviewer_keywords: ["ISettingsNamespace interface [SMI]","RemoveSettingByPath method","ISettingsNamespace.RemoveSettingByPath","ISettingsNamespace::RemoveSettingByPath","RemoveSettingByPath","RemoveSettingByPath method [SMI]","RemoveSettingByPath method [SMI]","ISettingsNamespace interface","smi.isettingsnamespace_removesettingbypath","wcmconfig/ISettingsNamespace::RemoveSettingByPath"]
old-location: smi\isettingsnamespace_removesettingbypath.htm
tech.root: SMI
ms.assetid: 6c2cf0be-9c9f-46d6-9108-47d2ad405645
ms.date: 12/05/2018
ms.keywords: ISettingsNamespace interface [SMI],RemoveSettingByPath method, ISettingsNamespace.RemoveSettingByPath, ISettingsNamespace::RemoveSettingByPath, RemoveSettingByPath, RemoveSettingByPath method [SMI], RemoveSettingByPath method [SMI],ISettingsNamespace interface, smi.isettingsnamespace_removesettingbypath, wcmconfig/ISettingsNamespace::RemoveSettingByPath
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
 - ISettingsNamespace::RemoveSettingByPath
 - wcmconfig/ISettingsNamespace::RemoveSettingByPath
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
 - ISettingsNamespace.RemoveSettingByPath
---

# ISettingsNamespace::RemoveSettingByPath


## -description

Removes the setting object specified by a path.

## -parameters

### -param Path [in]

The path of the setting object.

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
Indicates an attempt to remove an item that does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates an attempt to remove an element that is not in the list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, either because it is a read-only item, or the namespace was opened in ReadOnly mode.

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
<dt><b>WCM_E_WRONGESCAPESTRING </b></dt>
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
Indicates that the path is incorrectly specified and references the wrong key for the list item.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsnamespace">ISettingsNamespace</a>