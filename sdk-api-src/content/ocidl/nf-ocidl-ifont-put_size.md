---
UID: NF:ocidl.IFont.put_Size
title: IFont::put_Size (ocidl.h)
description: Sets the point size of the font.
helpviewer_keywords: ["IFont interface [COM]","put_Size method","IFont.put_Size","IFont::put_Size","_ctrl_ifont_put_size","com.ifont_put_size","ocidl/IFont::put_Size","put_Size","put_Size method [COM]","put_Size method [COM]","IFont interface"]
old-location: com\ifont_put_size.htm
tech.root: com
ms.assetid: 1c39a7dc-553b-41b7-8b66-1a5980493dce
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Size method, IFont.put_Size, IFont::put_Size, _ctrl_ifont_put_size, com.ifont_put_size, ocidl/IFont::put_Size, put_Size, put_Size method [COM], put_Size method [COM],IFont interface
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
 - IFont::put_Size
 - ocidl/IFont::put_Size
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
 - IFont.put_Size
---

# IFont::put_Size


## -description

Sets the point size of the font.

## -parameters

### -param size [in]

The new size of the font, in <b>HIMETRIC</b> units.

## -returns

The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the following values.

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
The font was resized successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>size</i> parameter is not valid. For example, it does not contain a usable font size.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_size">IFont::get_Size</a>