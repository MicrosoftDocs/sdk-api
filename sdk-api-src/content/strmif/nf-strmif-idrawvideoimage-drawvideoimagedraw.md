---
UID: NF:strmif.IDrawVideoImage.DrawVideoImageDraw
title: IDrawVideoImage::DrawVideoImageDraw (strmif.h)
description: Note  This interface has been deprecated. New applications should not use it. The DrawVideoImageDraw method draws the specified source rectangle to the specified destination rectangle in the specified GDI device context.helpviewer_keywords: ["DrawVideoImageDraw","DrawVideoImageDraw method [DirectShow]","DrawVideoImageDraw method [DirectShow]","IDrawVideoImage interface","IDrawVideoImage interface [DirectShow]","DrawVideoImageDraw method","IDrawVideoImage.DrawVideoImageDraw","IDrawVideoImage::DrawVideoImageDraw","IDrawVideoImageDrawVideoImageDraw","dshow.idrawvideoimage_drawvideoimagedraw","strmif/IDrawVideoImage::DrawVideoImageDraw"]
old-location: dshow\idrawvideoimage_drawvideoimagedraw.htm
tech.root: DirectShow
ms.assetid: cecc3ae4-f1fa-437e-b967-c54fca10b27c
ms.date: 12/05/2018
ms.keywords: DrawVideoImageDraw, DrawVideoImageDraw method [DirectShow], DrawVideoImageDraw method [DirectShow],IDrawVideoImage interface, IDrawVideoImage interface [DirectShow],DrawVideoImageDraw method, IDrawVideoImage.DrawVideoImageDraw, IDrawVideoImage::DrawVideoImageDraw, IDrawVideoImageDrawVideoImageDraw, dshow.idrawvideoimage_drawvideoimagedraw, strmif/IDrawVideoImage::DrawVideoImageDraw
f1_keywords:
- strmif/IDrawVideoImage.DrawVideoImageDraw
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IDrawVideoImage.DrawVideoImageDraw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDrawVideoImage::DrawVideoImageDraw


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>DrawVideoImageDraw</code> method draws the specified source rectangle to the specified destination rectangle in the specified GDI device context.




## -parameters




### -param hdc [in]

Specifies the device context.


### -param lprcSrc [in]

Pointer to a <b>RECT</b> structure that specifies the source rectangle, as a subrectangle of the current video frame.


### -param lprcDst [in]

Pointer to a <b>RECT</b> structure that specifies the destination rectangle in the device context.


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




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idrawvideoimage">IDrawVideoImage Interface</a>
 

 

