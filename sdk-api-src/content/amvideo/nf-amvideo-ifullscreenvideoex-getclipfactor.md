---
UID: NF:amvideo.IFullScreenVideoEx.GetClipFactor
title: IFullScreenVideoEx::GetClipFactor (amvideo.h)
description: The GetClipFactor method retrieves the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip. For example, if the clip factor is 25, the Full Screen Renderer can clip up to 25% of the video.
helpviewer_keywords: ["GetClipFactor","GetClipFactor method [DirectShow]","GetClipFactor method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetClipFactor method","IFullScreenVideoEx.GetClipFactor","IFullScreenVideoEx::GetClipFactor","IFullScreenVideoGetClipFactor","amvideo/IFullScreenVideoEx::GetClipFactor","dshow.ifullscreenvideoex_getclipfactor"]
old-location: dshow\ifullscreenvideoex_getclipfactor.htm
tech.root: dshow
ms.assetid: f45e1736-8130-483b-9f90-614c4b6970db
ms.date: 12/05/2018
ms.keywords: GetClipFactor, GetClipFactor method [DirectShow], GetClipFactor method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetClipFactor method, IFullScreenVideoEx.GetClipFactor, IFullScreenVideoEx::GetClipFactor, IFullScreenVideoGetClipFactor, amvideo/IFullScreenVideoEx::GetClipFactor, dshow.ifullscreenvideoex_getclipfactor
req.header: amvideo.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFullScreenVideoEx::GetClipFactor
 - amvideo/IFullScreenVideoEx::GetClipFactor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.GetClipFactor
---

# IFullScreenVideoEx::GetClipFactor


## -description

The <code>GetClipFactor</code> method retrieves the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip. For example, if the clip factor is 25, the Full Screen Renderer can clip up to 25% of the video.

## -parameters

### -param pClipFactor [out]

Pointer to a variable the receives the clip factor.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>