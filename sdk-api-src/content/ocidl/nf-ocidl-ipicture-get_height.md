---
UID: NF:ocidl.IPicture.get_Height
title: IPicture::get_Height (ocidl.h)
description: Retrieves the current height of the picture in the picture object.
helpviewer_keywords: ["IPicture interface [COM]","get_Height method","IPicture.get_Height","IPicture::get_Height","_ctrl_ipicture_get_height","com.ipicture_get_height","get_Height","get_Height method [COM]","get_Height method [COM]","IPicture interface","ocidl/IPicture::get_Height"]
old-location: com\ipicture_get_height.htm
tech.root: com
ms.assetid: a582cc9d-4356-49ec-9f14-38c75e690fbe
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_Height method, IPicture.get_Height, IPicture::get_Height, _ctrl_ipicture_get_height, com.ipicture_get_height, get_Height, get_Height method [COM], get_Height method [COM],IPicture interface, ocidl/IPicture::get_Height
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
 - IPicture::get_Height
 - ocidl/IPicture::get_Height
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
 - IPicture.get_Height
---

# IPicture::get_Height


## -description

Retrieves the current height of the picture in the picture object.

## -parameters

### -param pHeight [out]

A pointer to a variable that receives the height.

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
The height was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pHeight</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>