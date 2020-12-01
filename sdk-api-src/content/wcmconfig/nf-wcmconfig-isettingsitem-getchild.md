---
UID: NF:wcmconfig.ISettingsItem.GetChild
title: ISettingsItem::GetChild (wcmconfig.h)
description: Gets the child item that has the specified name.
helpviewer_keywords: ["GetChild","GetChild method [SMI]","GetChild method [SMI]","ISettingsItem interface","ISettingsItem interface [SMI]","GetChild method","ISettingsItem.GetChild","ISettingsItem::GetChild","smi.isettingsitem_getchild","wcmconfig/ISettingsItem::GetChild"]
old-location: smi\isettingsitem_getchild.htm
tech.root: SMI
ms.assetid: 4a3d3212-bd47-46fb-9ce1-79ac109c6444
ms.date: 12/05/2018
ms.keywords: GetChild, GetChild method [SMI], GetChild method [SMI],ISettingsItem interface, ISettingsItem interface [SMI],GetChild method, ISettingsItem.GetChild, ISettingsItem::GetChild, smi.isettingsitem_getchild, wcmconfig/ISettingsItem::GetChild
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
 - ISettingsItem::GetChild
 - wcmconfig/ISettingsItem::GetChild
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
 - ISettingsItem.GetChild
---

# ISettingsItem::GetChild


## -description

Gets the child item that has the specified name.

## -parameters

### -param Name [in]

The name of the child item.

### -param Child [out]

A pointer to an <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> object that corresponds to the child item.

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
Indicates that the requested name is not a child of the item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_WRONGESCAPESTRING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the name contains an unrecognized XML escape sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCM_E_INVALIDPATH</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the name is not formatted correctly.

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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the item does not support children.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a>