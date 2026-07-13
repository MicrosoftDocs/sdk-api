---
UID: NF:evr.IMFVideoDisplayControl.SetBorderColor
title: IMFVideoDisplayControl::SetBorderColor (evr.h)
description: Sets the border color for the video.
helpviewer_keywords: ["4a3647a8-4789-4f18-979b-4a9ee1ce7b71","IMFVideoDisplayControl interface [Media Foundation]","SetBorderColor method","IMFVideoDisplayControl.SetBorderColor","IMFVideoDisplayControl::SetBorderColor","SetBorderColor","SetBorderColor method [Media Foundation]","SetBorderColor method [Media Foundation]","IMFVideoDisplayControl interface","evr/IMFVideoDisplayControl::SetBorderColor","mf.imfvideodisplaycontrol_setbordercolor"]
old-location: mf\imfvideodisplaycontrol_setbordercolor.htm
tech.root: mfarchive
ms.assetid: 4a3647a8-4789-4f18-979b-4a9ee1ce7b71
ms.date: 12/05/2018
ms.keywords: 4a3647a8-4789-4f18-979b-4a9ee1ce7b71, IMFVideoDisplayControl interface [Media Foundation],SetBorderColor method, IMFVideoDisplayControl.SetBorderColor, IMFVideoDisplayControl::SetBorderColor, SetBorderColor, SetBorderColor method [Media Foundation], SetBorderColor method [Media Foundation],IMFVideoDisplayControl interface, evr/IMFVideoDisplayControl::SetBorderColor, mf.imfvideodisplaycontrol_setbordercolor
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoDisplayControl::SetBorderColor
 - evr/IMFVideoDisplayControl::SetBorderColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl.SetBorderColor
archived: true
---

# IMFVideoDisplayControl::SetBorderColor


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the border color for the video.

## -parameters

### -param Clr [in]

Specifies the border color as a <b>COLORREF</b> value.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>

## -remarks

By default, if the video window straddles two monitors, the enhanced video renderer (EVR) clips the video to one monitor and draws the border color on the remaining portion of the window. (To change the clipping behavior, call <a href="/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs">IMFVideoDisplayControl::SetRenderingPrefs</a>.)

The border color is not used for letterboxing. To change the letterbox color, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setbackgroundcolor">IMFVideoProcessor::SetBackgroundColor</a>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>