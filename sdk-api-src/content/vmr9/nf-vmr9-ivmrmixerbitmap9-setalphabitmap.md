---
UID: NF:vmr9.IVMRMixerBitmap9.SetAlphaBitmap
title: IVMRMixerBitmap9::SetAlphaBitmap (vmr9.h)
description: The SetAlphaBitmap method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.
helpviewer_keywords: ["IVMRMixerBitmap9 interface [DirectShow]","SetAlphaBitmap method","IVMRMixerBitmap9.SetAlphaBitmap","IVMRMixerBitmap9::SetAlphaBitmap","IVMRMixerBitmap9SetAlphaBitmap","SetAlphaBitmap","SetAlphaBitmap method [DirectShow]","SetAlphaBitmap method [DirectShow]","IVMRMixerBitmap9 interface","dshow.ivmrmixerbitmap9_setalphabitmap","vmr9/IVMRMixerBitmap9::SetAlphaBitmap"]
old-location: dshow\ivmrmixerbitmap9_setalphabitmap.htm
tech.root: dshow
ms.assetid: 22aadb5b-8dc8-48ec-bff1-1bac498f3984
ms.date: 4/26/2023
ms.keywords: IVMRMixerBitmap9 interface [DirectShow],SetAlphaBitmap method, IVMRMixerBitmap9.SetAlphaBitmap, IVMRMixerBitmap9::SetAlphaBitmap, IVMRMixerBitmap9SetAlphaBitmap, SetAlphaBitmap, SetAlphaBitmap method [DirectShow], SetAlphaBitmap method [DirectShow],IVMRMixerBitmap9 interface, dshow.ivmrmixerbitmap9_setalphabitmap, vmr9/IVMRMixerBitmap9::SetAlphaBitmap
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
 - IVMRMixerBitmap9::SetAlphaBitmap
 - vmr9/IVMRMixerBitmap9::SetAlphaBitmap
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
 - IVMRMixerBitmap9.SetAlphaBitmap
---

# IVMRMixerBitmap9::SetAlphaBitmap


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetAlphaBitmap</code> method specifies a new bitmap image and the source location of the bitmap and how and where it should be rendered on the destination rectangle.

## -parameters

### -param pBmpParms [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure that contains information about the bitmap.

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

To remove the bitmap, set the VMR9AlphaBitmap_Disable flag in the <b>VMR9AlphaBitmap</b> structure and call <code>SetAlphaBitmap</code> again.

The application can provide the bitmap either as a Direct3D surface or as a GDI bitmap. To use a Direct3D surface, set the <b>pDDS</b> member of the <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure. To use a GDI bitmap, set the <b>hdc</b> member of the structure.

The bitmap is mixed onto the video frame by the VMR's mixer component. The mixer draws the bitmap once per frame. If you change the bitmap while the filter graph is paused or stopped, the mixer does not use the new bitmap until the graph restarts. You can work around this limitation by calling <a href="/windows/desktop/api/control/nf-control-imediacontrol-stopwhenready">IMediaControl::StopWhenReady</a>, although a better solution is to write a custom allocator-presenter to draw the bitmap. For more information, see <a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-9">Supplying a Custom Allocator-Presenter for VMR-9</a>.

If the method returns E_INVALIDARG, possible reasons include the following:

<ul>
<li>The Direct3D surface was not allocated from the D3DPOOL_SYSTEMMEM pool.</li>
<li>Invalid surface format. If a Direct3D surface is used, the surface format must be D3DFMT_X8R8G8B8 or D3DFMT_A8R8G8B8. If the surface format is D3DFMT_A8R8G8B8, the VMR9AlphaBitmap_SrcColorKey flag cannot be used.</li>
<li>The source rectangle (rSrc) exceeds the boundaries of the Direct3D surface.</li>
<li>The source rectangle is empty.</li>
<li>The source rectangle exceeds the maximum texture width or maximum texture height for the Direct3D device. To find the maximum texture size, call <b>IDirect3DDevice9::GetDeviceCaps</b>.</li>
<li>The <b>dwFilterMode</b> member contains an invalid combination of flags.</li>
</ul>
Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixerbitmap9-getalphabitmapparameters">GetAlphaBitmapParameters</a>



<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixerbitmap9">IVMRMixerBitmap9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>