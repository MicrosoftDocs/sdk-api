---
UID: NF:vmr9.IVMRWindowlessControl9.GetNativeVideoSize
title: IVMRWindowlessControl9::GetNativeVideoSize (vmr9.h)
description: The GetNativeVideoSize method retrieves the un-stretched video size and aspect ratio of the video.
helpviewer_keywords: ["GetNativeVideoSize","GetNativeVideoSize method [DirectShow]","GetNativeVideoSize method [DirectShow]","IVMRWindowlessControl9 interface","IVMRWindowlessControl9 interface [DirectShow]","GetNativeVideoSize method","IVMRWindowlessControl9.GetNativeVideoSize","IVMRWindowlessControl9::GetNativeVideoSize","IVMRWindowlessControl9GetNativeVideoSize","dshow.ivmrwindowlesscontrol9_getnativevideosize","vmr9/IVMRWindowlessControl9::GetNativeVideoSize"]
old-location: dshow\ivmrwindowlesscontrol9_getnativevideosize.htm
tech.root: dshow
ms.assetid: 4e70c94e-7c20-4a4e-b276-feb7a9f9784c
ms.date: 4/26/2023
ms.keywords: GetNativeVideoSize, GetNativeVideoSize method [DirectShow], GetNativeVideoSize method [DirectShow],IVMRWindowlessControl9 interface, IVMRWindowlessControl9 interface [DirectShow],GetNativeVideoSize method, IVMRWindowlessControl9.GetNativeVideoSize, IVMRWindowlessControl9::GetNativeVideoSize, IVMRWindowlessControl9GetNativeVideoSize, dshow.ivmrwindowlesscontrol9_getnativevideosize, vmr9/IVMRWindowlessControl9::GetNativeVideoSize
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
 - IVMRWindowlessControl9::GetNativeVideoSize
 - vmr9/IVMRWindowlessControl9::GetNativeVideoSize
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
 - IVMRWindowlessControl9.GetNativeVideoSize
---

# IVMRWindowlessControl9::GetNativeVideoSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNativeVideoSize</code> method retrieves the un-stretched video size and aspect ratio of the video.

## -parameters

### -param lpWidth [out]

Pointer that receives the width of the native video rectangle.

### -param lpHeight [out]

Pointer that receives the height of the native video rectangle.

### -param lpARWidth [out]

Pointer that receives the aspect ratio width of the native video rectangle.

### -param lpARHeight [out]

Pointer that receives the aspect ratio height of the native video rectangle.

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

If the VMR is not connected to an upstream filter, this method will succeed but all parameters will be set to zero.

If <i>lpWidth</i> is 640 and <i>lpHeight</i> is 480, then <i>lpARWidth</i> will be 4 and <i>lpARHeight</i> will be 3.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>