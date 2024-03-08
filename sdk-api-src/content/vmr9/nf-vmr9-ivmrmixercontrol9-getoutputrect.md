---
UID: NF:vmr9.IVMRMixerControl9.GetOutputRect
title: IVMRMixerControl9::GetOutputRect (vmr9.h)
description: The GetOutputRect method retrieves the position of this stream's video rectangle within the composition rectangle.
helpviewer_keywords: ["GetOutputRect","GetOutputRect method [DirectShow]","GetOutputRect method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetOutputRect method","IVMRMixerControl9.GetOutputRect","IVMRMixerControl9::GetOutputRect","IVMRMixerControl9GetOutputRect","dshow.ivmrmixercontrol9_getoutputrect","vmr9/IVMRMixerControl9::GetOutputRect"]
old-location: dshow\ivmrmixercontrol9_getoutputrect.htm
tech.root: dshow
ms.assetid: 93d976a4-1c48-4aac-8326-92b1ad9b751c
ms.date: 4/26/2023
ms.keywords: GetOutputRect, GetOutputRect method [DirectShow], GetOutputRect method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetOutputRect method, IVMRMixerControl9.GetOutputRect, IVMRMixerControl9::GetOutputRect, IVMRMixerControl9GetOutputRect, dshow.ivmrmixercontrol9_getoutputrect, vmr9/IVMRMixerControl9::GetOutputRect
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
 - IVMRMixerControl9::GetOutputRect
 - vmr9/IVMRMixerControl9::GetOutputRect
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
 - IVMRMixerControl9.GetOutputRect
---

# IVMRMixerControl9::GetOutputRect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputRect</code> method retrieves the position of this stream's video rectangle within the composition rectangle.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param pRect [out]

Pointer to a <a href="/windows/win32/api/strmif/ns-strmif-normalizedrect">NORMALIZEDRECT</a> structure that receives the destination rectangle in composition space.

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
<i>pRect</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>

## -remarks

Because this rectangle exists in compositional space, there is no such thing as an "invalid" rectangle. For example, if left is greater than right, it means the video is mirrored in the x direction. An empty rectangle turns off this stream.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>