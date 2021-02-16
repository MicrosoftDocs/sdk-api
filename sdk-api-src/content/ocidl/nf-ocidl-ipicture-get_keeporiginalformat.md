---
UID: NF:ocidl.IPicture.get_KeepOriginalFormat
title: IPicture::get_KeepOriginalFormat (ocidl.h)
description: Retrieves the current value of the picture's KeepOriginalFormat property.
helpviewer_keywords: ["IPicture interface [COM]","get_KeepOriginalFormat method","IPicture.get_KeepOriginalFormat","IPicture::get_KeepOriginalFormat","_ctrl_ipicture_get_keeporiginalformat","com.ipicture_get_keeporiginalformat","get_KeepOriginalFormat","get_KeepOriginalFormat method [COM]","get_KeepOriginalFormat method [COM]","IPicture interface","ocidl/IPicture::get_KeepOriginalFormat"]
old-location: com\ipicture_get_keeporiginalformat.htm
tech.root: com
ms.assetid: 90befcb7-138f-4c63-a6ec-ec06c89b3317
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_KeepOriginalFormat method, IPicture.get_KeepOriginalFormat, IPicture::get_KeepOriginalFormat, _ctrl_ipicture_get_keeporiginalformat, com.ipicture_get_keeporiginalformat, get_KeepOriginalFormat, get_KeepOriginalFormat method [COM], get_KeepOriginalFormat method [COM],IPicture interface, ocidl/IPicture::get_KeepOriginalFormat
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
 - IPicture::get_KeepOriginalFormat
 - ocidl/IPicture::get_KeepOriginalFormat
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
 - IPicture.get_KeepOriginalFormat
---

# IPicture::get_KeepOriginalFormat


## -description

Retrieves the current value of the picture's KeepOriginalFormat property.

## -parameters

### -param pKeep [out]

A pointer to a variable that receives the value of the property.

## -returns

This method supports the standard return value E_FAIL, as well as the following value.

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
The value of the KeepOriginalFormat property was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pKeep</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-put_keeporiginalformat">IPicture::put_KeepOriginalFormat</a>