---
UID: NF:ocidl.IFont.put_Italic
title: IFont::put_Italic (ocidl.h)
description: Sets the font's Italic property.
helpviewer_keywords: ["IFont interface [COM]","put_Italic method","IFont.put_Italic","IFont::put_Italic","_ctrl_ifont_put_italic","com.ifont_put_italic","ocidl/IFont::put_Italic","put_Italic","put_Italic method [COM]","put_Italic method [COM]","IFont interface"]
old-location: com\ifont_put_italic.htm
tech.root: com
ms.assetid: a59169e1-d3c4-4dc0-b228-afad0e4d4307
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Italic method, IFont.put_Italic, IFont::put_Italic, _ctrl_ifont_put_italic, com.ifont_put_italic, ocidl/IFont::put_Italic, put_Italic, put_Italic method [COM], put_Italic method [COM],IFont interface
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
 - IFont::put_Italic
 - ocidl/IFont::put_Italic
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
 - IFont.put_Italic
---

# IFont::put_Italic


## -description

Sets the font's Italic property.

## -parameters

### -param italic [in]

The new Italic property for the font.

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
The italic state was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support an italic state. This value is not an error condition.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_italic">IFont::get_Italic</a>