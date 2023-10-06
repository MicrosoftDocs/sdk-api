---
UID: NF:strmif.IDDrawExclModeVideo.GetNativeVideoProps
title: IDDrawExclModeVideo::GetNativeVideoProps (strmif.h)
description: The GetNativeVideoProps method retrieves the current video size and picture aspect ratio of the Overlay Mixer's primary stream.
helpviewer_keywords: ["GetNativeVideoProps","GetNativeVideoProps method [DirectShow]","GetNativeVideoProps method [DirectShow]","IDDrawExclModeVideo interface","IDDrawExclModeVideo interface [DirectShow]","GetNativeVideoProps method","IDDrawExclModeVideo.GetNativeVideoProps","IDDrawExclModeVideo::GetNativeVideoProps","IDDrawExclModeVideoGetNativeVideoProps","dshow.iddrawexclmodevideo_getnativevideoprops","strmif/IDDrawExclModeVideo::GetNativeVideoProps"]
old-location: dshow\iddrawexclmodevideo_getnativevideoprops.htm
tech.root: dshow
ms.assetid: cc6b3f73-bfb4-4a71-b3e9-53345abd1430
ms.date: 4/26/2023
ms.keywords: GetNativeVideoProps, GetNativeVideoProps method [DirectShow], GetNativeVideoProps method [DirectShow],IDDrawExclModeVideo interface, IDDrawExclModeVideo interface [DirectShow],GetNativeVideoProps method, IDDrawExclModeVideo.GetNativeVideoProps, IDDrawExclModeVideo::GetNativeVideoProps, IDDrawExclModeVideoGetNativeVideoProps, dshow.iddrawexclmodevideo_getnativevideoprops, strmif/IDDrawExclModeVideo::GetNativeVideoProps
req.header: strmif.h
req.include-header: Dshow.h
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
 - IDDrawExclModeVideo::GetNativeVideoProps
 - strmif/IDDrawExclModeVideo::GetNativeVideoProps
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
 - IDDrawExclModeVideo.GetNativeVideoProps
---

# IDDrawExclModeVideo::GetNativeVideoProps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNativeVideoProps</code> method retrieves the current video size and picture aspect ratio of the Overlay Mixer's primary stream.

## -parameters

### -param pdwVideoWidth [out]

Address of variable that receives the width of the video.

### -param pdwVideoHeight [out]

Address of variable that receives the height of the video.

### -param pdwPictAspectRatioX [out]

Address of variable that receives the x-axis aspect ratio.

### -param pdwPictAspectRatioY [out]

Address of variable that receives the y-axis aspect ratio.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

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
</table>

## -remarks

The filter graph should look for the <a href="/windows/desktop/DirectShow/ec-video-size-changed">EC_VIDEO_SIZE_CHANGED</a> event, and on its receipt call this method to adjust the aspect ratio and position.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>