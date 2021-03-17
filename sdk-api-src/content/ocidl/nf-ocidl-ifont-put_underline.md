---
UID: NF:ocidl.IFont.put_Underline
title: IFont::put_Underline (ocidl.h)
description: Sets the font's Underline property.
helpviewer_keywords: ["IFont interface [COM]","put_Underline method","IFont.put_Underline","IFont::put_Underline","_ctrl_ifont_put_underline","com.ifont_put_underline","ocidl/IFont::put_Underline","put_Underline","put_Underline method [COM]","put_Underline method [COM]","IFont interface"]
old-location: com\ifont_put_underline.htm
tech.root: com
ms.assetid: c763c050-cf69-4c9d-83a9-66ccc1d4376c
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],put_Underline method, IFont.put_Underline, IFont::put_Underline, _ctrl_ifont_put_underline, com.ifont_put_underline, ocidl/IFont::put_Underline, put_Underline, put_Underline method [COM], put_Underline method [COM],IFont interface
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
 - IFont::put_Underline
 - ocidl/IFont::put_Underline
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
 - IFont.put_Underline
---

# IFont::put_Underline


## -description

Sets the font's Underline property.

## -parameters

### -param underline [in]

The new Underline property for the font.

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
The underline state was changed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font does not support an underline state. This value is not an error condition.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_underline">IFont::get_Underline</a>