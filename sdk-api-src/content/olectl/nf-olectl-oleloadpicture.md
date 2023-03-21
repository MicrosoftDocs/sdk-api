---
UID: NF:olectl.OleLoadPicture
title: OleLoadPicture function (olectl.h)
description: Creates a new picture object and initializes it from the contents of a stream. This is equivalent to calling OleCreatePictureIndirect with NULL as the first parameter, followed by a call to IPersistStream::Load. (OleLoadPicture)
helpviewer_keywords: ["OleLoadPicture","OleLoadPicture function [COM]","_ole_OleLoadPicture","com.oleloadpicture","olectl/OleLoadPicture"]
old-location: com\oleloadpicture.htm
tech.root: com
ms.assetid: de1847cd-ecc0-4941-9dbc-a60b8ef0b1c1
ms.date: 12/05/2018
ms.keywords: OleLoadPicture, OleLoadPicture function [COM], _ole_OleLoadPicture, com.oleloadpicture, olectl/OleLoadPicture
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleLoadPicture
 - olectl/OleLoadPicture
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleLoadPicture
---

# OleLoadPicture function


## -description

Creates a new picture object and initializes it from the contents of a stream. This is equivalent to calling <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> with <b>NULL</b> as the first parameter, followed by a call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a>.

## -parameters

### -param lpstream [in]

Pointer to the stream that contains the picture's data.

### -param lSize [in]

The number of bytes that should be read from the stream, or zero if the entire stream should be read.

### -param fRunmode [in]

The opposite of the initial value of the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_keeporiginalformat">KeepOriginalFormat</a> property. If <b>TRUE</b>, <a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-put_keeporiginalformat">KeepOriginalFormat</a> is set to <b>FALSE</b> and vice-versa.

### -param riid [in]

Reference to the identifier of the interface describing the type of interface pointer to return in <i>ppvObj</i>.

### -param lplpvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the storage of the object identified by the moniker. If *<i>ppvObj</i> is non-<b>NULL</b>, this function calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a> on the interface; it is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>. If an error occurs, *<i>ppvObj</i> is set to <b>NULL</b>.

## -returns

This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The stream is not valid. For example, it may be <b>NULL</b>.


</td>
</tr>
</table>

## -remarks

The stream must be in BMP (bitmap), WMF (metafile), or ICO (icon) format. A picture object created using <b>OleLoadPicture</b> always has ownership of its internal resources (<i>fOwn</i>==<b>TRUE</b> is implied).

## -see-also

<a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>



<a href="/windows/desktop/api/olectl/ns-olectl-pictdesc">PICTDESC</a>
