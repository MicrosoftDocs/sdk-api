---
UID: NF:ocidl.IPicture.get_Width
title: IPicture::get_Width (ocidl.h)
description: Retrieves the current width of the picture in the picture object.
helpviewer_keywords: ["IPicture interface [COM]","get_Width method","IPicture.get_Width","IPicture::get_Width","_ctrl_ipicture_get_width","com.ipicture_get_width","get_Width","get_Width method [COM]","get_Width method [COM]","IPicture interface","ocidl/IPicture::get_Width"]
old-location: com\ipicture_get_width.htm
tech.root: com
ms.assetid: d69443ed-143c-4477-8602-50f919119b0f
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_Width method, IPicture.get_Width, IPicture::get_Width, _ctrl_ipicture_get_width, com.ipicture_get_width, get_Width, get_Width method [COM], get_Width method [COM],IPicture interface, ocidl/IPicture::get_Width
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
 - IPicture::get_Width
 - ocidl/IPicture::get_Width
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
 - IPicture.get_Width
---

# IPicture::get_Width


## -description

Retrieves the current width of the picture in the picture object.

## -parameters

### -param pWidth [out]

A pointer to a variable that receives the width.

## -returns

This method supports the standard return value E_FAIL, as well as the following values.

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
The width was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pWidth</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>