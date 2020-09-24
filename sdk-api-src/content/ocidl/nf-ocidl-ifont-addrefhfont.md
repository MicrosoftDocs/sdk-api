---
UID: NF:ocidl.IFont.AddRefHfont
title: IFont::AddRefHfont (ocidl.h)
description: Notifies the font object that the previously realized font identified with hFont should remain valid until ReleaseHfont is called or the font object itself is released completely.
helpviewer_keywords: ["AddRefHfont","AddRefHfont method [COM]","AddRefHfont method [COM]","IFont interface","IFont interface [COM]","AddRefHfont method","IFont.AddRefHfont","IFont::AddRefHfont","_ctrl_ifont_addrefhfont","com.ifont_addrefhfont","ocidl/IFont::AddRefHfont"]
old-location: com\ifont_addrefhfont.htm
tech.root: com
ms.assetid: f86d52b8-e763-4948-b853-039721ae9b38
ms.date: 12/05/2018
ms.keywords: AddRefHfont, AddRefHfont method [COM], AddRefHfont method [COM],IFont interface, IFont interface [COM],AddRefHfont method, IFont.AddRefHfont, IFont::AddRefHfont, _ctrl_ifont_addrefhfont, com.ifont_addrefhfont, ocidl/IFont::AddRefHfont
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
 - IFont::AddRefHfont
 - ocidl/IFont::AddRefHfont
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
 - IFont.AddRefHfont
---

# IFont::AddRefHfont


## -description

Notifies the font object that the previously realized font identified with <i>hFont</i> should remain valid until <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-releasehfont">ReleaseHfont</a> is called or the font object itself is released completely.

## -parameters

### -param hFont [in]

Font handle previously realized through <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_hfont">get_hFont</a> to be locked in the font object's cache.

## -returns

The method supports the standard return values <b>E_UNEXPECTED</b> and <b>E_INVALIDARG</b>, as well as the following values.

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
The font was successfully locked in the cache.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-releasehfont">ReleaseHfont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_hfont">get_hFont</a>