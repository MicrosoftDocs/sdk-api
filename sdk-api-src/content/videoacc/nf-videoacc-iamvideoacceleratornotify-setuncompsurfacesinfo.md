---
UID: NF:videoacc.IAMVideoAcceleratorNotify.SetUncompSurfacesInfo
title: IAMVideoAcceleratorNotify::SetUncompSurfacesInfo (videoacc.h)
description: The SetUncompSurfacesInfo method notifies the decoder of how many uncompressed surfaces were created.
helpviewer_keywords: ["IAMVideoAcceleratorNotify interface [DirectShow]","SetUncompSurfacesInfo method","IAMVideoAcceleratorNotify.SetUncompSurfacesInfo","IAMVideoAcceleratorNotify::SetUncompSurfacesInfo","IAMVideoAcceleratorNotifySetUncompSurfacesInfo","SetUncompSurfacesInfo","SetUncompSurfacesInfo method [DirectShow]","SetUncompSurfacesInfo method [DirectShow]","IAMVideoAcceleratorNotify interface","dshow.iamvideoacceleratornotify_setuncompsurfacesinfo","videoacc/IAMVideoAcceleratorNotify::SetUncompSurfacesInfo"]
old-location: dshow\iamvideoacceleratornotify_setuncompsurfacesinfo.htm
tech.root: dshow
ms.assetid: e82c73e6-d32e-4875-9f9d-124a1c6ce504
ms.date: 4/26/2023
ms.keywords: IAMVideoAcceleratorNotify interface [DirectShow],SetUncompSurfacesInfo method, IAMVideoAcceleratorNotify.SetUncompSurfacesInfo, IAMVideoAcceleratorNotify::SetUncompSurfacesInfo, IAMVideoAcceleratorNotifySetUncompSurfacesInfo, SetUncompSurfacesInfo, SetUncompSurfacesInfo method [DirectShow], SetUncompSurfacesInfo method [DirectShow],IAMVideoAcceleratorNotify interface, dshow.iamvideoacceleratornotify_setuncompsurfacesinfo, videoacc/IAMVideoAcceleratorNotify::SetUncompSurfacesInfo
req.header: videoacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMVideoAcceleratorNotify::SetUncompSurfacesInfo
 - videoacc/IAMVideoAcceleratorNotify::SetUncompSurfacesInfo
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
 - IAMVideoAcceleratorNotify.SetUncompSurfacesInfo
---

# IAMVideoAcceleratorNotify::SetUncompSurfacesInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetUncompSurfacesInfo</b> method notifies the decoder of how many uncompressed surfaces were created.

## -parameters

### -param dwActualUncompSurfacesAllocated [in]

The number of surfaces allocated.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. <b>HRESULT</b> can include one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

The video renderer calls this method after it allocates uncompressed surfaces for video decoding.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-reference">DirectShow Reference</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-decoders-use-iamvideoaccelerator">How Decoders Use IAMVideoAccelerator</a>



<a href="/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify">IAMVideoAcceleratorNotify Interface</a>