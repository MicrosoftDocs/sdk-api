---
UID: NF:strmif.IVMRMixerBitmap.GetAlphaBitmapParameters
title: IVMRMixerBitmap::GetAlphaBitmapParameters (strmif.h)
description: The GetAlphaBitmapParameters method retrieves a copy of the current image and related blending parameters.
helpviewer_keywords: ["GetAlphaBitmapParameters","GetAlphaBitmapParameters method [DirectShow]","GetAlphaBitmapParameters method [DirectShow]","IVMRMixerBitmap interface","IVMRMixerBitmap interface [DirectShow]","GetAlphaBitmapParameters method","IVMRMixerBitmap.GetAlphaBitmapParameters","IVMRMixerBitmap::GetAlphaBitmapParameters","IVMRMixerBitmapGetAlphaBitmapParameters","dshow.ivmrmixerbitmap_getalphabitmapparameters","strmif/IVMRMixerBitmap::GetAlphaBitmapParameters"]
old-location: dshow\ivmrmixerbitmap_getalphabitmapparameters.htm
tech.root: dshow
ms.assetid: d03cc6ad-e09b-4af7-93b7-51880465c0b6
ms.date: 4/26/2023
ms.keywords: GetAlphaBitmapParameters, GetAlphaBitmapParameters method [DirectShow], GetAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap interface, IVMRMixerBitmap interface [DirectShow],GetAlphaBitmapParameters method, IVMRMixerBitmap.GetAlphaBitmapParameters, IVMRMixerBitmap::GetAlphaBitmapParameters, IVMRMixerBitmapGetAlphaBitmapParameters, dshow.ivmrmixerbitmap_getalphabitmapparameters, strmif/IVMRMixerBitmap::GetAlphaBitmapParameters
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRMixerBitmap::GetAlphaBitmapParameters
 - strmif/IVMRMixerBitmap::GetAlphaBitmapParameters
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
 - IVMRMixerBitmap.GetAlphaBitmapParameters
---

# IVMRMixerBitmap::GetAlphaBitmapParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAlphaBitmapParameters</b> method retrieves a copy of the current image and related blending parameters.

## -parameters

### -param pBmpParms [out]

A pointer to a [VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure that receives the bitmap, information about the blending values, and the location to blend it.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

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
<i>pBmpParms</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mixer has not been loaded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap">IVMRMixerBitmap::SetAlphaBitmap</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a>