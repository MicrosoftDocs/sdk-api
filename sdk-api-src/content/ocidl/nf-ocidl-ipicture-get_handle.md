---
UID: NF:ocidl.IPicture.get_Handle
title: IPicture::get_Handle (ocidl.h)
description: Retrieves the handle to the picture managed within this picture object to a specified location.
helpviewer_keywords: ["IPicture interface [COM]","get_Handle method","IPicture.get_Handle","IPicture::get_Handle","_ctrl_ipicture_get_handle","com.ipicture_get_handle","get_Handle","get_Handle method [COM]","get_Handle method [COM]","IPicture interface","ocidl/IPicture::get_Handle"]
old-location: com\ipicture_get_handle.htm
tech.root: com
ms.assetid: 196b911b-a685-44d5-a772-a71767f957f5
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_Handle method, IPicture.get_Handle, IPicture::get_Handle, _ctrl_ipicture_get_handle, com.ipicture_get_handle, get_Handle, get_Handle method [COM], get_Handle method [COM],IPicture interface, ocidl/IPicture::get_Handle
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
 - IPicture::get_Handle
 - ocidl/IPicture::get_Handle
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
 - IPicture.get_Handle
---

# IPicture::get_Handle


## -description

Retrieves the handle to the picture managed within this picture object to a specified location.

## -parameters

### -param pHandle [out]

A pointer to a variable that receives the handle. The caller is responsible for this handle upon successful return. The variable is set to <b>NULL</b> on failure.

## -returns

This method supports the standard return values E_FAIL and E_OUTOFMEMORY, as well as the following values.

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
The handle was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>phandle</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers_"></a><a id="notes_to_callers_"></a><a id="NOTES_TO_CALLERS_"></a>Notes to Callers
</h3>
The picture object may retain ownership of the picture. However, the caller can be assured that the picture will remain valid until either the caller specifically destroys the picture or the picture object is itself destroyed. The <i>fOwn</i> parameter to <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> determines ownership when the picture object is created. <a href="/windows/desktop/api/olectl/nf-olectl-oleloadpicture">OleLoadPicture</a> forces <i>fOwn</i> to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>