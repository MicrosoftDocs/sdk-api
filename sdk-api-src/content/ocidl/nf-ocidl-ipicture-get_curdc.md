---
UID: NF:ocidl.IPicture.get_CurDC
title: IPicture::get_CurDC (ocidl.h)
description: Retrieves the handle of the current device context. This property is valid only for bitmap pictures.
helpviewer_keywords: ["IPicture interface [COM]","get_CurDC method","IPicture.get_CurDC","IPicture::get_CurDC","_ctrl_ipicture_get_curdc","com.ipicture_get_curdc","get_CurDC","get_CurDC method [COM]","get_CurDC method [COM]","IPicture interface","ocidl/IPicture::get_CurDC"]
old-location: com\ipicture_get_curdc.htm
tech.root: com
ms.assetid: a5c13a54-692d-423f-824d-5a96c137dec9
ms.date: 12/05/2018
ms.keywords: IPicture interface [COM],get_CurDC method, IPicture.get_CurDC, IPicture::get_CurDC, _ctrl_ipicture_get_curdc, com.ipicture_get_curdc, get_CurDC, get_CurDC method [COM], get_CurDC method [COM],IPicture interface, ocidl/IPicture::get_CurDC
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
 - IPicture::get_CurDC
 - ocidl/IPicture::get_CurDC
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
 - IPicture.get_CurDC
---

# IPicture::get_CurDC


## -description

Retrieves the handle of the current device context. This property is valid only for bitmap pictures.

## -parameters

### -param phDC [out]

A pointer a variable that receives the device context.

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
The value of <i>phDC</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The CurDC property and the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-selectpicture">IPicture::SelectPicture</a> method exist to circumvent restrictions in Windows; specifically, that an object can only be selected into exactly one device context at a time. In some cases, a picture object may be permanently selected into a particular device context (for example, a control may use a certain picture for a background). To use this picture property elsewhere, it must be temporarily deselected from its old device context, selected into the new device context for the operation, then reselected back into the old device context. The <b>IPicture::get_CurDC</b> method returns the device context handle into which the picture is currently selected. The <b>IPicture::SelectPicture</b> method selects the picture into a new device context, returning the old device context and the picture's GDI handle. The caller should select the picture back into the old device context when the caller is done with it, as is normal for Windows code.

<h3><a id="Notes_to_Callers_"></a><a id="notes_to_callers_"></a><a id="NOTES_TO_CALLERS_"></a>Notes to Callers
</h3>
The caller always owns any device contexts passed between it and the picture object. Because the picture object maintains a copy of the HDC, the caller should use a memory device context (created with the <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> function) and not a screen device context (from <a href="/windows/desktop/api/winuser/nf-winuser-getdc">GetDC</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdca">CreateDC</a>, or <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>), because the screen device contexts are a limited system resource.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipicture">IPicture</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipicture-selectpicture">IPicture::SelectPicture</a>