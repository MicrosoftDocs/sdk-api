---
UID: NF:evr9.IMFVideoMixerBitmap.GetAlphaBitmapParameters
title: IMFVideoMixerBitmap::GetAlphaBitmapParameters (evr9.h)
description: Retrieves the current settings that the enhanced video renderer (EVR) uses to alpha-blend the bitmap with the video.
helpviewer_keywords: ["0361e340-9de7-47f3-80fd-61d5e914d44e","GetAlphaBitmapParameters","GetAlphaBitmapParameters method [Media Foundation]","GetAlphaBitmapParameters method [Media Foundation]","IMFVideoMixerBitmap interface","IMFVideoMixerBitmap interface [Media Foundation]","GetAlphaBitmapParameters method","IMFVideoMixerBitmap.GetAlphaBitmapParameters","IMFVideoMixerBitmap::GetAlphaBitmapParameters","evr9/IMFVideoMixerBitmap::GetAlphaBitmapParameters","mf.imfvideomixerbitmap_getalphabitmapparameters"]
old-location: mf\imfvideomixerbitmap_getalphabitmapparameters.htm
tech.root: mfarchive
ms.assetid: 0361e340-9de7-47f3-80fd-61d5e914d44e
ms.date: 12/05/2018
ms.keywords: 0361e340-9de7-47f3-80fd-61d5e914d44e, GetAlphaBitmapParameters, GetAlphaBitmapParameters method [Media Foundation], GetAlphaBitmapParameters method [Media Foundation],IMFVideoMixerBitmap interface, IMFVideoMixerBitmap interface [Media Foundation],GetAlphaBitmapParameters method, IMFVideoMixerBitmap.GetAlphaBitmapParameters, IMFVideoMixerBitmap::GetAlphaBitmapParameters, evr9/IMFVideoMixerBitmap::GetAlphaBitmapParameters, mf.imfvideomixerbitmap_getalphabitmapparameters
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoMixerBitmap::GetAlphaBitmapParameters
 - evr9/IMFVideoMixerBitmap::GetAlphaBitmapParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoMixerBitmap.GetAlphaBitmapParameters
archived: true
---

# IMFVideoMixerBitmap::GetAlphaBitmapParameters


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves the current settings that the enhanced video renderer (EVR) uses to alpha-blend the bitmap with the video.

## -parameters

### -param pBmpParms [out]

Pointer to an <a href="/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmapparams">MFVideoAlphaBitmapParams</a> structure that receives the current blending parameters.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No bitmap is currently set. You must call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap">IMFVideoMixerBitmap::SetAlphaBitmap</a> to set a bitmap.

</td>
</tr>
</table>

## -remarks

This method returns the current values of all the blending parameters, not just those that the application specified. Ignore the <b>dwFlags</b> member of the structure.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap">IMFVideoMixerBitmap</a>