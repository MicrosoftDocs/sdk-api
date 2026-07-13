---
UID: NF:vmr9.IVMRMixerBitmap9.GetAlphaBitmapParameters
title: IVMRMixerBitmap9::GetAlphaBitmapParameters (vmr9.h)
description: The GetAlphaBitmapParameters method retrieves a copy of the current image and related blending parameters.
helpviewer_keywords: ["GetAlphaBitmapParameters","GetAlphaBitmapParameters method [DirectShow]","GetAlphaBitmapParameters method [DirectShow]","IVMRMixerBitmap9 interface","IVMRMixerBitmap9 interface [DirectShow]","GetAlphaBitmapParameters method","IVMRMixerBitmap9.GetAlphaBitmapParameters","IVMRMixerBitmap9::GetAlphaBitmapParameters","IVMRMixerBitmap9GetAlphaBitmapParameters","dshow.ivmrmixerbitmap9_getalphabitmapparameters","vmr9/IVMRMixerBitmap9::GetAlphaBitmapParameters"]
old-location: dshow\ivmrmixerbitmap9_getalphabitmapparameters.htm
tech.root: dshow
ms.assetid: a5e5891f-6842-40e7-8bf4-29c6979c7551
ms.date: 4/26/2023
ms.keywords: GetAlphaBitmapParameters, GetAlphaBitmapParameters method [DirectShow], GetAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap9 interface, IVMRMixerBitmap9 interface [DirectShow],GetAlphaBitmapParameters method, IVMRMixerBitmap9.GetAlphaBitmapParameters, IVMRMixerBitmap9::GetAlphaBitmapParameters, IVMRMixerBitmap9GetAlphaBitmapParameters, dshow.ivmrmixerbitmap9_getalphabitmapparameters, vmr9/IVMRMixerBitmap9::GetAlphaBitmapParameters
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
 - IVMRMixerBitmap9::GetAlphaBitmapParameters
 - vmr9/IVMRMixerBitmap9::GetAlphaBitmapParameters
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
 - IVMRMixerBitmap9.GetAlphaBitmapParameters
---

# IVMRMixerBitmap9::GetAlphaBitmapParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAlphaBitmapParameters</code> method retrieves a copy of the current image and related blending parameters.

## -parameters

### -param pBmpParms [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure that receives the bitmap, information about the blending values, and the location to blend it.

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

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixerbitmap9">IVMRMixerBitmap9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>