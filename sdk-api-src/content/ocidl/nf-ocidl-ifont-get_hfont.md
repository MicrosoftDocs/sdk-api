---
UID: NF:ocidl.IFont.get_hFont
title: IFont::get_hFont (ocidl.h)
description: Retrieves a handle to the font described by this font object.
helpviewer_keywords: ["IFont interface [COM]","get_hFont method","IFont.get_hFont","IFont::get_hFont","_ctrl_ifont_get_hfont","com.ifont_get_hfont","get_hFont","get_hFont method [COM]","get_hFont method [COM]","IFont interface","ocidl/IFont::get_hFont"]
old-location: com\ifont_get_hfont.htm
tech.root: com
ms.assetid: 19bfd78a-0e81-45c3-a3b8-bc893669e9f5
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],get_hFont method, IFont.get_hFont, IFont::get_hFont, _ctrl_ifont_get_hfont, com.ifont_get_hfont, get_hFont, get_hFont method [COM], get_hFont method [COM],IFont interface, ocidl/IFont::get_hFont
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
 - IFont::get_hFont
 - ocidl/IFont::get_hFont
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
 - IFont.get_hFont
---

# IFont::get_hFont


## -description

Retrieves a handle to the font described by this font object.

## -parameters

### -param phFont [out]

A pointer to the caller-allocated variable that receives the font handle. 
      The caller does not own this resource and must not attempt to destroy the font.

## -returns

The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_OUTOFMEMORY</b>, as well as the following values.

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
The font handle was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in the <i>phFont</i> parameter is not valid. For example, it may be 
        <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The font object maintains ownership of the <b>HFONT</b> and can destroy it 
    at any time without prior notification. If the caller needs to secure this font for a limited period of time, it 
    can call <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-addrefhfont">IFont::AddRefHfont</a> and 
    <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-releasehfont">IFont::ReleaseHfont</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-addrefhfont">IFont::AddRefHfont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-releasehfont">IFont::ReleaseHfont</a>