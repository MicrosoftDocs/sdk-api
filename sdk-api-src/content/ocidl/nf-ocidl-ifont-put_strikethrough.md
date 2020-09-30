---
UID: NF:ocidl.IFont.put_Strikethrough
title: IFont::put_Strikethrough (ocidl.h)
description: Sets the font's Strikethrough property.
helpviewer_keywords: ["IFont interface [COM]","put_Strikethrough method","IFont.put_Strikethrough","IFont::put_Strikethrough","_ctrl_ifont_put_strikethrough","com.ifont_put_strikethrough","ocidl/IFont::put_Strikethrough","put_Strikethrough","put_Strikethrough method [COM]","put_Strikethrough method [COM]","IFont interface"]
old-location: com\ifont_put_strikethrough.htm
tech.root: com
ms.assetid: 32b9c3aa-4c89-441e-9b41-0ac6d8a52bba
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Strikethrough method, IFont.put_Strikethrough, IFont::put_Strikethrough, _ctrl_ifont_put_strikethrough, com.ifont_put_strikethrough, ocidl/IFont::put_Strikethrough, put_Strikethrough, put_Strikethrough method [COM], put_Strikethrough method [COM],IFont interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFont::put_Strikethrough
 - ocidl/IFont::put_Strikethrough
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IFont.put_Strikethrough
---

# IFont::put_Strikethrough


## -description

Sets the font's Strikethrough property.

## -parameters

### -param strikethrough [in]

The new Strikethrough property for the font.

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
The Strikethrough property was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support a strikethrough state. This value is not an error condition.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_strikethrough">IFont::get_Strikethrough</a>