---
UID: NF:ocidl.IFont.get_Charset
title: IFont::get_Charset (ocidl.h)
description: Retrieves the character set used in the font.
helpviewer_keywords: ["IFont interface [COM]","get_Charset method","IFont.get_Charset","IFont::get_Charset","_ctrl_ifont_get_charset","com.ifont_get_charset","get_Charset","get_Charset method [COM]","get_Charset method [COM]","IFont interface","ocidl/IFont::get_Charset"]
old-location: com\ifont_get_charset.htm
tech.root: com
ms.assetid: 3a784453-db29-4917-90ee-8893f787646a
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],get_Charset method, IFont.get_Charset, IFont::get_Charset, _ctrl_ifont_get_charset, com.ifont_get_charset, get_Charset, get_Charset method [COM], get_Charset method [COM],IFont interface, ocidl/IFont::get_Charset
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
 - IFont::get_Charset
 - ocidl/IFont::get_Charset
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
 - IFont.get_Charset
---

# IFont::get_Charset


## -description

Retrieves the character set used in the font. The character set can be any of those defined 
   for Windows fonts.

## -parameters

### -param pCharset [out]

A pointer to the caller-allocated variable that receives the character set 
      value.

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
The character set was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pCharset</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_charset">IFont::put_Charset</a>