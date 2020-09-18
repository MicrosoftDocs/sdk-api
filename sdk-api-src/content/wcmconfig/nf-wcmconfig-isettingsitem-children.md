---
UID: NF:wcmconfig.ISettingsItem.Children
title: ISettingsItem::Children (wcmconfig.h)
description: Gets the dictionary of the child items that correspond to this item.
helpviewer_keywords: ["Children","Children method [SMI]","Children method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","Children method","ISettingsItem.Children","ISettingsItem::Children","smi.isettingsitem_children","wcmconfig/ISettingsItem::Children"]
old-location: smi\isettingsitem_children.htm
tech.root: SMI
ms.assetid: 33bd7f91-c414-420e-bc18-1114924b93e9
ms.date: 12/05/2018
ms.keywords: Children, Children method [SMI], Children method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],Children method, ISettingsItem.Children, ISettingsItem::Children, smi.isettingsitem_children, wcmconfig/ISettingsItem::Children
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
 - ISettingsItem::Children
 - wcmconfig/ISettingsItem::Children
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
 - ISettingsItem.Children
---

# ISettingsItem::Children


## -description

Gets the dictionary of the child items that correspond to this item.

## -parameters

### -param Children [out]

An <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-iitemenumerator">IItemEnumerator</a> interface pointer used to access the children.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that there are insufficient resources to allocate an enumerator for the children.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item does not support having children.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>