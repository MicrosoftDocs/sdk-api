---
UID: NF:wcmconfig.ISettingsItem.GetListKeyInformation
title: ISettingsItem::GetListKeyInformation (wcmconfig.h)
description: Gets the list information for this item.
helpviewer_keywords: ["GetListKeyInformation","GetListKeyInformation method [SMI]","GetListKeyInformation method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetListKeyInformation method","ISettingsItem.GetListKeyInformation","ISettingsItem::GetListKeyInformation","smi.isettingsitem_getlistkeyinformation","wcmconfig/ISettingsItem::GetListKeyInformation"]
old-location: smi\isettingsitem_getlistkeyinformation.htm
tech.root: SMI
ms.assetid: 34ee8457-34d1-4eff-813b-f59c35c4aa95
ms.date: 12/05/2018
ms.keywords: GetListKeyInformation, GetListKeyInformation method [SMI], GetListKeyInformation method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetListKeyInformation method, ISettingsItem.GetListKeyInformation, ISettingsItem::GetListKeyInformation, smi.isettingsitem_getlistkeyinformation, wcmconfig/ISettingsItem::GetListKeyInformation
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
 - ISettingsItem::GetListKeyInformation
 - wcmconfig/ISettingsItem::GetListKeyInformation
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
 - ISettingsItem.GetListKeyInformation
---

# ISettingsItem::GetListKeyInformation


## -description

Gets the list information for this item.

## -parameters

### -param KeyName [out]

The name of the key.

### -param DataType [out]

A <a href="/windows/win32/api/wcmconfig/ne-wcmconfig-wcmdatatype">WcmDataType</a> value that indicates the data type of the item.

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
<dt><b>S_FALSE </b></dt>
</dl>
</td>
<td width="60%">
Indicates that the list is keyed by keyValue, and  KeyName is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item is not a list or list element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there are insufficient resources to complete the operation. 

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>