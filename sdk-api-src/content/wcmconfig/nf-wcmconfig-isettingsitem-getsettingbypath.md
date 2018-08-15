---
UID: NF:wcmconfig.ISettingsItem.GetSettingByPath
title: ISettingsItem::GetSettingByPath
author: windows-sdk-content
description: Gets a setting based on the given path.
old-location: smi\isettingsitem_getsettingbypath.htm
old-project: smi
ms.assetid: a4270c46-b214-4232-b414-d6b6e4e35635
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSettingByPath, GetSettingByPath method [SMI], GetSettingByPath method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetSettingByPath method, ISettingsItem.GetSettingByPath, ISettingsItem::GetSettingByPath, smi.isettingsitem_getsettingbypath, wcmconfig/ISettingsItem::GetSettingByPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.redist: 
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
 - ISettingsItem.GetSettingByPath
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsItem::GetSettingByPath


## -description


Gets a setting based on the given path.


## -parameters




### -param Path [in]

Path of the list element or attribute to retrieve. The path is relative to the current setting.


### -param Setting [out]

 An <a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a> interface pointer used to access the item.


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




<a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a>
 

 

