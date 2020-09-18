---
UID: NF:ocidl.IPicture.get_Attributes
title: IPicture::get_Attributes (ocidl.h)
description: Retrieves the current set of the picture's bit attributes.
helpviewer_keywords: ["IPicture interface [COM]","get_Attributes method","IPicture.get_Attributes","IPicture::get_Attributes","_ctrl_ipicture_get_attributes","com.ipicture_get_attributes","get_Attributes","get_Attributes method [COM]","get_Attributes method [COM]","IPicture interface","ocidl/IPicture::get_Attributes"]
old-location: com\ipicture_get_attributes.htm
tech.root: com
ms.assetid: ed71f0eb-3af4-463f-93e1-29d5dd1cc684
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_Attributes method, IPicture.get_Attributes, IPicture::get_Attributes, _ctrl_ipicture_get_attributes, com.ipicture_get_attributes, get_Attributes, get_Attributes method [COM], get_Attributes method [COM],IPicture interface, ocidl/IPicture::get_Attributes
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
 - IPicture::get_Attributes
 - ocidl/IPicture::get_Attributes
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
 - IPicture.get_Attributes
---

# IPicture::get_Attributes


## -description

Retrieves the current set of the picture's bit attributes.

## -parameters

### -param pDwAttr [out]

A pointer to a variable that receives the value of the Attributes property.

The Attributes property can contain any combination of the values from the <a href="/windows/desktop/api/ocidl/ne-ocidl-pictureattributes">PICTUREATTRIBUTES</a> enumeration.

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
The attribute bits were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pdwAttr</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-pictureattributes">PICTUREATTRIBUTES</a>