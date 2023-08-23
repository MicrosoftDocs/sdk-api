---
UID: NF:strmif.IVMRWindowlessControl.GetCurrentImage
title: IVMRWindowlessControl::GetCurrentImage (strmif.h)
description: The GetCurrentImage method retrieves a copy of the current image being displayed by the VMR.
helpviewer_keywords: ["GetCurrentImage","GetCurrentImage method [DirectShow]","GetCurrentImage method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetCurrentImage method","IVMRWindowlessControl.GetCurrentImage","IVMRWindowlessControl::GetCurrentImage","IVMRWindowlessControlGetCurrentImage","dshow.ivmrwindowlesscontrol_getcurrentimage","strmif/IVMRWindowlessControl::GetCurrentImage"]
old-location: dshow\ivmrwindowlesscontrol_getcurrentimage.htm
tech.root: dshow
ms.assetid: 515e252d-4ac4-49ec-8d94-bf850dd4783f
ms.date: 4/26/2023
ms.keywords: GetCurrentImage, GetCurrentImage method [DirectShow], GetCurrentImage method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetCurrentImage method, IVMRWindowlessControl.GetCurrentImage, IVMRWindowlessControl::GetCurrentImage, IVMRWindowlessControlGetCurrentImage, dshow.ivmrwindowlesscontrol_getcurrentimage, strmif/IVMRWindowlessControl::GetCurrentImage
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRWindowlessControl::GetCurrentImage
 - strmif/IVMRWindowlessControl::GetCurrentImage
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
 - IVMRWindowlessControl.GetCurrentImage
---

# IVMRWindowlessControl::GetCurrentImage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentImage</code> method retrieves a copy of the current image being displayed by the VMR.

## -parameters

### -param lpDib [out]

Address of a pointer to a BYTE array.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>

## -remarks

This method returns the current image being displayed. The image is returned in the form of packed Windows DIB. The image starts with a <b>BITMAPINFOHEADER</b> structure, possibly including palette entries and/or color masks, followed by the image data.

The VMR allocates the memory for the image and returns a pointer to it in the <i>lpDib</i> variable. The caller must free the memory by calling <b>CoTaskMemFree</b>.

This method can be called at any time, no matter what state the filter is in, whether running, stopped or paused. However, frequent calls to this method will degrade video playback performance.


#### Examples

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BYTE *lpDib = NULL;
hr = pWindowlessControl-&gt;GetCurrentImage(&amp;lpDib);
if (SUCCEEDED(hr))
{
    BITMAPINFOHEADER *pBMIH = (BITMAPINFOHEADER*)lpDib;
    /* .... */
    CoTaskMemFree(lpDib);
}</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>