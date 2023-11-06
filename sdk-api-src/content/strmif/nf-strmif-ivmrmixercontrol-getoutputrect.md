---
UID: NF:strmif.IVMRMixerControl.GetOutputRect
title: IVMRMixerControl::GetOutputRect (strmif.h)
description: The GetOutputRect method retrieves the position of this stream's video rectangle within the composition rectangle.
helpviewer_keywords: ["GetOutputRect","GetOutputRect method [DirectShow]","GetOutputRect method [DirectShow]","IVMRMixerControl interface","IVMRMixerControl interface [DirectShow]","GetOutputRect method","IVMRMixerControl.GetOutputRect","IVMRMixerControl::GetOutputRect","IVMRMixerControlGetOutputRect","dshow.ivmrmixercontrol_getoutputrect","strmif/IVMRMixerControl::GetOutputRect"]
old-location: dshow\ivmrmixercontrol_getoutputrect.htm
tech.root: dshow
ms.assetid: da6409b0-161d-4724-b448-e68cb5d1941c
ms.date: 4/26/2023
ms.keywords: GetOutputRect, GetOutputRect method [DirectShow], GetOutputRect method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetOutputRect method, IVMRMixerControl.GetOutputRect, IVMRMixerControl::GetOutputRect, IVMRMixerControlGetOutputRect, dshow.ivmrmixercontrol_getoutputrect, strmif/IVMRMixerControl::GetOutputRect
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
 - IVMRMixerControl::GetOutputRect
 - strmif/IVMRMixerControl::GetOutputRect
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
 - IVMRMixerControl.GetOutputRect
---

# IVMRMixerControl::GetOutputRect


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOutputRect</code> method retrieves the position of this stream's video rectangle within the composition rectangle.

## -parameters

### -param dwStreamID [in]

Specifies the input stream.

### -param pRect [out]

Pointer to a [NORMALIZEDRECT](/windows/win32/api/strmif/ns-strmif-normalizedrect) structure that receives the destination rectangle in composition space.

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

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-setmixingprefs">IVMRMixerControl::SetOutputRect</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>