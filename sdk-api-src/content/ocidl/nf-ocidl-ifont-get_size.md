---
UID: NF:ocidl.IFont.get_Size
title: IFont::get_Size (ocidl.h)
description: Retrieves the point size of the font.
helpviewer_keywords: ["IFont interface [COM]","get_Size method","IFont.get_Size","IFont::get_Size","_ctrl_ifont_get_size","com.ifont_get_size","get_Size","get_Size method [COM]","get_Size method [COM]","IFont interface","ocidl/IFont::get_Size"]
old-location: com\ifont_get_size.htm
tech.root: com
ms.assetid: aeee7dfc-5ccd-4c30-a59e-5eec93505288
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],get_Size method, IFont.get_Size, IFont::get_Size, _ctrl_ifont_get_size, com.ifont_get_size, get_Size, get_Size method [COM], get_Size method [COM],IFont interface, ocidl/IFont::get_Size
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
 - IFont::get_Size
 - ocidl/IFont::get_Size
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
 - IFont.get_Size
---

# IFont::get_Size


## -description

Retrieves the point size of the font.

## -parameters

### -param pSize [out]

 A pointer to the caller-allocated variable that receives the size,  in <b>HIMETRIC</b> 
   units.

## -returns

The method supports the standard return value <b>E_UNEXPECTED</b>, as well as the 
      following values.

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
The size was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>pSize</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-put_size">IFont::put_Size</a>