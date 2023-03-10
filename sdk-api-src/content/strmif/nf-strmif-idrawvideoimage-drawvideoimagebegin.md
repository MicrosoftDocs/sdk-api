---
UID: NF:strmif.IDrawVideoImage.DrawVideoImageBegin
title: IDrawVideoImage::DrawVideoImageBegin (strmif.h)
description: Note  This interface has been deprecated. New applications should not use it. The DrawVideoImageBegin method turns off DirectDraw in preparation for a call to the DrawVideoImageDraw method.
helpviewer_keywords: ["DrawVideoImageBegin","DrawVideoImageBegin method [DirectShow]","DrawVideoImageBegin method [DirectShow]","IDrawVideoImage interface","IDrawVideoImage interface [DirectShow]","DrawVideoImageBegin method","IDrawVideoImage.DrawVideoImageBegin","IDrawVideoImage::DrawVideoImageBegin","IDrawVideoImageDrawVideoImageBegin","dshow.idrawvideoimage_drawvideoimagebegin","strmif/IDrawVideoImage::DrawVideoImageBegin"]
old-location: dshow\idrawvideoimage_drawvideoimagebegin.htm
tech.root: dshow
ms.assetid: a39125b3-15b1-428d-aa64-c1b2bccf616a
ms.date: 12/05/2018
ms.keywords: DrawVideoImageBegin, DrawVideoImageBegin method [DirectShow], DrawVideoImageBegin method [DirectShow],IDrawVideoImage interface, IDrawVideoImage interface [DirectShow],DrawVideoImageBegin method, IDrawVideoImage.DrawVideoImageBegin, IDrawVideoImage::DrawVideoImageBegin, IDrawVideoImageDrawVideoImageBegin, dshow.idrawvideoimage_drawvideoimagebegin, strmif/IDrawVideoImage::DrawVideoImageBegin
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IDrawVideoImage::DrawVideoImageBegin
 - strmif/IDrawVideoImage::DrawVideoImageBegin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDrawVideoImage.DrawVideoImageBegin
---

# IDrawVideoImage::DrawVideoImageBegin


## -description

<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>DrawVideoImageBegin</code> method turns off DirectDraw in preparation for a call to the <b>DrawVideoImageDraw</b> method.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-idrawvideoimage">IDrawVideoImage Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idrawvideoimage-drawvideoimagedraw">IDrawVideoImage::DrawVideoImageDraw</a>
