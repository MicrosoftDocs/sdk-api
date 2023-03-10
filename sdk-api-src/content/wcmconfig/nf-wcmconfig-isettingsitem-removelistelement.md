---
UID: NF:wcmconfig.ISettingsItem.RemoveListElement
title: ISettingsItem::RemoveListElement (wcmconfig.h)
description: Removes an existing list element of the supplied name.
helpviewer_keywords: ["ISettingsItem interface [SMI]","RemoveListElement method","ISettingsItem.RemoveListElement","ISettingsItem::RemoveListElement","RemoveListElement","RemoveListElement method [SMI]","RemoveListElement method [SMI]","ISettingsItem interface","smi.isettingsitem_removelistelement","wcmconfig/ISettingsItem::RemoveListElement"]
old-location: smi\isettingsitem_removelistelement.htm
tech.root: SMI
ms.assetid: 4dca22b5-b4e3-4bb6-9eb4-5507472b63b2
ms.date: 12/05/2018
ms.keywords: ISettingsItem interface [SMI],RemoveListElement method, ISettingsItem.RemoveListElement, ISettingsItem::RemoveListElement, RemoveListElement, RemoveListElement method [SMI], RemoveListElement method [SMI],ISettingsItem interface, smi.isettingsitem_removelistelement, wcmconfig/ISettingsItem::RemoveListElement
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
 - ISettingsItem::RemoveListElement
 - wcmconfig/ISettingsItem::RemoveListElement
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
 - ISettingsItem.RemoveListElement
---

# ISettingsItem::RemoveListElement


## -description

Removes an existing list element of the supplied name.There cannot be multiples with same name because the name must be unique. If an item of the specified name is not present, the method returns <b>WCM_E_STATENOTNOTFOUND</b>.

## -parameters

### -param ElementName [in]

The name of the element to be removed.

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
<dt><b>WCM_E_STATENODENOTFOUND </b></dt>
</dl>
</td>
<td width="60%">
Indicates an attempt to remove an item that does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item that is not of setting type list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_READONLYITEM </b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item cannot be written, either because  it is a read-only item, or because the namespace was opened in ReadOnly mode.

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