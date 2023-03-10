---
UID: NF:ocidl.IFont.get_Italic
title: IFont::get_Italic (ocidl.h)
description: Gets the font's current Italic property.
helpviewer_keywords: ["IFont interface [COM]","get_Italic method","IFont.get_Italic","IFont::get_Italic","_ctrl_ifont_get_italic","com.ifont_get_italic","get_Italic","get_Italic method [COM]","get_Italic method [COM]","IFont interface","ocidl/IFont::get_Italic"]
old-location: com\ifont_get_italic.htm
tech.root: com
ms.assetid: d56c21d6-1296-4c0c-a13e-8e4b3164e747
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],get_Italic method, IFont.get_Italic, IFont::get_Italic, _ctrl_ifont_get_italic, com.ifont_get_italic, get_Italic, get_Italic method [COM], get_Italic method [COM],IFont interface, ocidl/IFont::get_Italic
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
 - IFont::get_Italic
 - ocidl/IFont::get_Italic
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
 - IFont.get_Italic
---

# IFont::get_Italic


## -description

Gets the font's current Italic property.

## -parameters

### -param pItalic [out]

A pointer to the caller-allocated variable that receives the current Italic property for the font.

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
The state was retrieved successfully. If the state is indeterminate, a font object should set 
        *<i>pItalic</i> to <b>FALSE</b> and return 
        <b>S_OK</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in pitalic is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_italic">IFont::put_Italic</a>