---
UID: NF:evr.IMFVideoDisplayControl.SetAspectRatioMode
title: IMFVideoDisplayControl::SetAspectRatioMode (evr.h)
description: Specifies how the enhanced video renderer (EVR) handles the aspect ratio of the source video.
helpviewer_keywords: ["IMFVideoDisplayControl interface [Media Foundation]","SetAspectRatioMode method","IMFVideoDisplayControl.SetAspectRatioMode","IMFVideoDisplayControl::SetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [Media Foundation]","SetAspectRatioMode method [Media Foundation]","IMFVideoDisplayControl interface","dd49a110-1c11-4eca-9e7b-6021f3bdd397","evr/IMFVideoDisplayControl::SetAspectRatioMode","mf.imfvideodisplaycontrol_setaspectratiomode"]
old-location: mf\imfvideodisplaycontrol_setaspectratiomode.htm
tech.root: mfarchive
ms.assetid: dd49a110-1c11-4eca-9e7b-6021f3bdd397
ms.date: 12/05/2018
ms.keywords: IMFVideoDisplayControl interface [Media Foundation],SetAspectRatioMode method, IMFVideoDisplayControl.SetAspectRatioMode, IMFVideoDisplayControl::SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [Media Foundation], SetAspectRatioMode method [Media Foundation],IMFVideoDisplayControl interface, dd49a110-1c11-4eca-9e7b-6021f3bdd397, evr/IMFVideoDisplayControl::SetAspectRatioMode, mf.imfvideodisplaycontrol_setaspectratiomode
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
 - IMFVideoDisplayControl::SetAspectRatioMode
 - evr/IMFVideoDisplayControl::SetAspectRatioMode
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
 - IMFVideoDisplayControl.SetAspectRatioMode
archived: true
---

# IMFVideoDisplayControl::SetAspectRatioMode


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Specifies how the enhanced video renderer (EVR) handles the aspect ratio of the source video.

## -parameters

### -param dwAspectRatioMode [in]

Bitwise <b>OR</b> of one or more flags from the <a href="/windows/desktop/api/evr/ne-evr-mfvideoaspectratiomode">MFVideoAspectRatioMode</a> enumeration.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid flags.

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

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol">IMFVideoDisplayControl</a>



<a href="/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>