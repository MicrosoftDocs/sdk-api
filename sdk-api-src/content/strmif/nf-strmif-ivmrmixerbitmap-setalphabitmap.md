---
UID: NF:strmif.IVMRMixerBitmap.SetAlphaBitmap
title: IVMRMixerBitmap::SetAlphaBitmap (strmif.h)
description: The SetAlphaBitmap method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.
helpviewer_keywords: ["IVMRMixerBitmap interface [DirectShow]","SetAlphaBitmap method","IVMRMixerBitmap.SetAlphaBitmap","IVMRMixerBitmap::SetAlphaBitmap","IVMRMixerBitmapSetAlphaBitmap","SetAlphaBitmap","SetAlphaBitmap method [DirectShow]","SetAlphaBitmap method [DirectShow]","IVMRMixerBitmap interface","dshow.ivmrmixerbitmap_setalphabitmap","strmif/IVMRMixerBitmap::SetAlphaBitmap"]
old-location: dshow\ivmrmixerbitmap_setalphabitmap.htm
tech.root: dshow
ms.assetid: 92e57c3a-6761-4a54-83f5-0ea0ce80d60b
ms.date: 4/26/2023
ms.keywords: IVMRMixerBitmap interface [DirectShow],SetAlphaBitmap method, IVMRMixerBitmap.SetAlphaBitmap, IVMRMixerBitmap::SetAlphaBitmap, IVMRMixerBitmapSetAlphaBitmap, SetAlphaBitmap, SetAlphaBitmap method [DirectShow], SetAlphaBitmap method [DirectShow],IVMRMixerBitmap interface, dshow.ivmrmixerbitmap_setalphabitmap, strmif/IVMRMixerBitmap::SetAlphaBitmap
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
 - IVMRMixerBitmap::SetAlphaBitmap
 - strmif/IVMRMixerBitmap::SetAlphaBitmap
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
 - IVMRMixerBitmap.SetAlphaBitmap
---

# IVMRMixerBitmap::SetAlphaBitmap


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAlphaBitmap</b> method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.

## -parameters

### -param pBmpParms [in]

A pointer to a [VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure that contains information about the bitmap.

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
<i>pBmpParms</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not create a destination DC or DIBSection for the bitmap.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
BitBlt to bitmap surface failed.

</td>
</tr>
</table>

## -remarks

To remove the bitmap, set the [VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure and call <b>SetAlphaBitmap</b> again.

The method might return <b>E_INVALIDARG</b> for several reasons:

<ul>
[VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure contains an invalid combination of flags.</li>
[VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure does not specify a valid HDC or DirectDraw surface.</li>
<li>The value of <b>fAlpha</b> is invalid.</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixerbitmap-getalphabitmapparameters">IVMRMixerBitmap::GetAlphaBitmapParameters</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a>