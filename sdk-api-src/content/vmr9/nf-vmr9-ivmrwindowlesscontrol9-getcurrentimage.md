---
UID: NF:vmr9.IVMRWindowlessControl9.GetCurrentImage
title: IVMRWindowlessControl9::GetCurrentImage (vmr9.h)
description: The GetCurrentImage method retrieves a copy of the current image being displayed by the VMR.
helpviewer_keywords: ["GetCurrentImage","GetCurrentImage method [DirectShow]","GetCurrentImage method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetCurrentImage method","IVMRWindowlessControl9.GetCurrentImage","IVMRWindowlessControl9::GetCurrentImage","IVMRWindowlessControl9GetCurrentImage","dshow.ivmrwindowlesscontrol9_getcurrentimage","vmr9/IVMRWindowlessControl9::GetCurrentImage"]
old-location: dshow\ivmrwindowlesscontrol9_getcurrentimage.htm
tech.root: dshow
ms.assetid: dddba9a5-be25-4dc4-9d91-eaff78d2405d
ms.date: 4/26/2023
ms.keywords: GetCurrentImage, GetCurrentImage method [DirectShow], GetCurrentImage method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetCurrentImage method, IVMRWindowlessControl9.GetCurrentImage, IVMRWindowlessControl9::GetCurrentImage, IVMRWindowlessControl9GetCurrentImage, dshow.ivmrwindowlesscontrol9_getcurrentimage, vmr9/IVMRWindowlessControl9::GetCurrentImage
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRWindowlessControl9::GetCurrentImage
 - vmr9/IVMRWindowlessControl9::GetCurrentImage
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
 - IVMRWindowlessControl9.GetCurrentImage
---

# IVMRWindowlessControl9::GetCurrentImage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurrentImage</code> method retrieves a copy of the current image being displayed by the VMR.

## -parameters

### -param lpDib [out]

Address of a pointer to a BYTE that will receive the DIB.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in windowless mode.

</td>
</tr>
</table>

## -remarks

This method returns the current image being displayed. The image is returned in the form of packed Windows DIB. The image starts with a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure, possibly including palette entries and/or color masks, followed by the image data.

The VMR allocates the memory for the image and returns a pointer to it in the <i>lpDib</i> variable. The caller must free the memory by calling <b>CoTaskMemFree</b>.

This method can be called at any time, no matter what state the filter is in, whether running, stopped or paused. However, frequent calls to this method will degrade video playback performance.

Include DShow.h and D3d9.h before Vmr9.h.


#### Examples


```cpp

BYTE *lpDib = NULL;
hr = pWindowlessControl->GetCurrentImage(&lpDib);
if (SUCCEEDED(hr))
{
    BITMAPINFOHEADER  *pBMIH = (BITMAPINFOHEADER*) lpDib;
    /* .... */
    CoTaskMemFree(lpDib);
}


```

## -see-also

<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>