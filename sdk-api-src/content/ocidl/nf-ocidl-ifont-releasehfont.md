---
UID: NF:ocidl.IFont.ReleaseHfont
title: IFont::ReleaseHfont (ocidl.h)
description: Notifies the font object that the caller that previously locked this font in the cache with IFont::AddRefHfont no longer requires the lock.
helpviewer_keywords: ["IFont interface [COM]","ReleaseHfont method","IFont.ReleaseHfont","IFont::ReleaseHfont","ReleaseHfont","ReleaseHfont method [COM]","ReleaseHfont method [COM]","IFont interface","_ctrl_ifont_releasehfont","com.ifont_releasehfont","ocidl/IFont::ReleaseHfont"]
old-location: com\ifont_releasehfont.htm
tech.root: com
ms.assetid: 2c2cf2e0-d0c8-4e4f-ba5a-6b08650aee68
ms.date: 12/05/2018
ms.keywords: IFont interface [COM],ReleaseHfont method, IFont.ReleaseHfont, IFont::ReleaseHfont, ReleaseHfont, ReleaseHfont method [COM], ReleaseHfont method [COM],IFont interface, _ctrl_ifont_releasehfont, com.ifont_releasehfont, ocidl/IFont::ReleaseHfont
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
 - IFont::ReleaseHfont
 - ocidl/IFont::ReleaseHfont
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
 - IFont.ReleaseHfont
---

# IFont::ReleaseHfont


## -description

Notifies the font object that the caller that previously locked this font in the cache with 
   <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-addrefhfont">IFont::AddRefHfont</a> no longer requires the lock.

## -parameters

### -param hFont [in]

A font handle previously realized through 
      <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-get_hfont">IFont::get_hFont</a>. This value was passed to a previous 
      call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-addrefhfont">IFont::AddRefHfont</a> to lock the font, and the 
      caller would now like to unlock the font in the cache.

## -returns

The method supports the standard return values <b>E_UNEXPECTED</b> and 
      <b>E_INVALIDARG</b>, as well as the following values.

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
The font was unlocked successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The font was not locked in the cache. This return value is a benign notification to the caller that it 
        may have a font reference counting problem.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ifont">IFont</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ifont-addrefhfont">IFont::AddRefHfont</a>