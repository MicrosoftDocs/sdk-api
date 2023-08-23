---
UID: NF:strmif.IVMRMixerControl.SetAlpha
title: IVMRMixerControl::SetAlpha (strmif.h)
description: The SetAlpha method sets a constant alpha value that is applied to this video stream.
helpviewer_keywords: ["IVMRMixerControl interface [DirectShow]","SetAlpha method","IVMRMixerControl.SetAlpha","IVMRMixerControl::SetAlpha","IVMRMixerControlSetAlpha","SetAlpha","SetAlpha method [DirectShow]","SetAlpha method [DirectShow]","IVMRMixerControl interface","dshow.ivmrmixercontrol_setalpha","strmif/IVMRMixerControl::SetAlpha"]
old-location: dshow\ivmrmixercontrol_setalpha.htm
tech.root: dshow
ms.assetid: aab95d45-b8f1-40cb-811f-c1d00aa37c97
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl interface [DirectShow],SetAlpha method, IVMRMixerControl.SetAlpha, IVMRMixerControl::SetAlpha, IVMRMixerControlSetAlpha, SetAlpha, SetAlpha method [DirectShow], SetAlpha method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setalpha, strmif/IVMRMixerControl::SetAlpha
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
 - IVMRMixerControl::SetAlpha
 - strmif/IVMRMixerControl::SetAlpha
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
 - IVMRMixerControl.SetAlpha
---

# IVMRMixerControl::SetAlpha


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetAlpha</code> method sets a constant alpha value that is applied to this video stream.

## -parameters

### -param dwStreamID [in]

Specifies the input stream.

### -param Alpha [in]

Specifies the alpha blending value to be applied to all the pixels in this stream.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>

## -remarks

The alpha value specified can be between 0.0 (fully transparent) and 1.0 (full opaque).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-getalpha">IVMRMixerControl::GetAlpha</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>