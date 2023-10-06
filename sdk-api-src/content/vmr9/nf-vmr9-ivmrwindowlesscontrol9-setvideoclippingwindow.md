---
UID: NF:vmr9.IVMRWindowlessControl9.SetVideoClippingWindow
title: IVMRWindowlessControl9::SetVideoClippingWindow (vmr9.h)
description: The SetVideoClippingWindow method specifies the container window that video should be clipped to.
helpviewer_keywords: ["IVMRWindowlessControl9 interface [DirectShow]","SetVideoClippingWindow method","IVMRWindowlessControl9.SetVideoClippingWindow","IVMRWindowlessControl9::SetVideoClippingWindow","IVMRWindowlessControl9SetVideoClippingWindow","SetVideoClippingWindow","SetVideoClippingWindow method [DirectShow]","SetVideoClippingWindow method [DirectShow]","IVMRWindowlessControl9 interface","dshow.ivmrwindowlesscontrol9_setvideoclippingwindow","vmr9/IVMRWindowlessControl9::SetVideoClippingWindow"]
old-location: dshow\ivmrwindowlesscontrol9_setvideoclippingwindow.htm
tech.root: dshow
ms.assetid: 426476cd-a7e9-42ef-9d1b-5bbf921557ed
ms.date: 4/26/2023
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetVideoClippingWindow method, IVMRWindowlessControl9.SetVideoClippingWindow, IVMRWindowlessControl9::SetVideoClippingWindow, IVMRWindowlessControl9SetVideoClippingWindow, SetVideoClippingWindow, SetVideoClippingWindow method [DirectShow], SetVideoClippingWindow method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setvideoclippingwindow, vmr9/IVMRWindowlessControl9::SetVideoClippingWindow
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
 - IVMRWindowlessControl9::SetVideoClippingWindow
 - vmr9/IVMRWindowlessControl9::SetVideoClippingWindow
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
 - IVMRWindowlessControl9.SetVideoClippingWindow
---

# IVMRWindowlessControl9::SetVideoClippingWindow


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetVideoClippingWindow</code> method specifies the container window that video should be clipped to.

## -parameters

### -param hwnd [in]

Specifies the window to which the video should be clipped.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>hwnd</i> parameter is <b>NULL</b>.

</td>
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

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>