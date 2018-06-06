---
UID: NF:wcmconfig.ISettingsNamespace.CreateSettingByPath
title: ISettingsNamespace::CreateSettingByPath
author: windows-sdk-content
description: Creates a setting object specified by its path.
old-location: smi\isettingsnamespace_createsettingbypath.htm
old-project: SMI
ms.assetid: 804cab32-eb0a-4e6e-8f58-042c1f5dde77
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateSettingByPath, CreateSettingByPath method [SMI], CreateSettingByPath method [SMI],ISettingsNamespace interface, ISettingsNamespace interface [SMI],CreateSettingByPath method, ISettingsNamespace.CreateSettingByPath, ISettingsNamespace::CreateSettingByPath, smi.isettingsnamespace_createsettingbypath, wcmconfig/ISettingsNamespace::CreateSettingByPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsNamespace.CreateSettingByPath
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsNamespace::CreateSettingByPath


## -description


Creates a setting object specified by its path.


## -parameters




### -param Path [in]

The path of the setting object.


### -param Setting [out]

A pointer to an <a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a> object that represents 
      the created setting.


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
Indicates an attempt to create a new item that is not a list element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDVALUE, WCM_E_INVALIDVALUEFORMAT, or WCM_E_INVALIDDATATYPE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an attempt to create a list item where the value provided for the key cannot be coerced to the 
        appropriate type. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, either because  it is a read-only item, or because the 
        namespace was opened in ReadOnly mode.

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
 




## -see-also




<a href="https://msdn.microsoft.com/a5d7b9ff-eb6f-40be-b246-17189cad92be">ISettingsNamespace</a>
 

 

