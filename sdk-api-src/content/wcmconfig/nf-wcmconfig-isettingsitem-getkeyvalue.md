---
UID: NF:wcmconfig.ISettingsItem.GetKeyValue
title: ISettingsItem::GetKeyValue (wcmconfig.h)
description: Extracts key values for any list that already exists in the image, for example, DNS, http settings, and user account information.
helpviewer_keywords: ["GetKeyValue","GetKeyValue method [SMI]","GetKeyValue method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetKeyValue method","ISettingsItem.GetKeyValue","ISettingsItem::GetKeyValue","smi.isettingsitem_getkeyvalue","wcmconfig/ISettingsItem::GetKeyValue"]
old-location: smi\isettingsitem_getkeyvalue.htm
tech.root: SMI
ms.assetid: a627d0aa-05ef-43b6-a8e8-bb0770dd8873
ms.date: 12/05/2018
ms.keywords: GetKeyValue, GetKeyValue method [SMI], GetKeyValue method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetKeyValue method, ISettingsItem.GetKeyValue, ISettingsItem::GetKeyValue, smi.isettingsitem_getkeyvalue, wcmconfig/ISettingsItem::GetKeyValue
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
 - ISettingsItem::GetKeyValue
 - wcmconfig/ISettingsItem::GetKeyValue
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
 - ISettingsItem.GetKeyValue
---

# ISettingsItem::GetKeyValue


## -description

Extracts key values for any list that already exists in the image, for example, DNS, http settings, and user account information.

## -parameters

### -param Value [out]

The value of the key for the list element. The type of the value returned is the actual type of the key. For example, the type is a string in the case of a dynamically keyed list. The value is unescaped appropriately to reverse the changes made by SMI for the purpose of storing it. The VARIANT type is overwritten with the correct type if the predefined VARIANT type is incorrect.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
The item is not a list element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There are insufficient resources to return information to the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value is null. 

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>