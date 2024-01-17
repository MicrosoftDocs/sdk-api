---
UID: NF:evr.IEVRTrustedVideoPlugin.SetConstriction
title: IEVRTrustedVideoPlugin::SetConstriction (evr.h)
description: Limits the effective video resolution.
helpviewer_keywords: ["IEVRTrustedVideoPlugin interface [Media Foundation]","SetConstriction method","IEVRTrustedVideoPlugin.SetConstriction","IEVRTrustedVideoPlugin::SetConstriction","SetConstriction","SetConstriction method [Media Foundation]","SetConstriction method [Media Foundation]","IEVRTrustedVideoPlugin interface","evr/IEVRTrustedVideoPlugin::SetConstriction","f2e9b199-969f-453c-8714-fa85c89a191a","mf.ievrtrustedvideoplugin_setconstriction"]
old-location: mf\ievrtrustedvideoplugin_setconstriction.htm
tech.root: mfarchive
ms.assetid: f2e9b199-969f-453c-8714-fa85c89a191a
ms.date: 12/05/2018
ms.keywords: IEVRTrustedVideoPlugin interface [Media Foundation],SetConstriction method, IEVRTrustedVideoPlugin.SetConstriction, IEVRTrustedVideoPlugin::SetConstriction, SetConstriction, SetConstriction method [Media Foundation], SetConstriction method [Media Foundation],IEVRTrustedVideoPlugin interface, evr/IEVRTrustedVideoPlugin::SetConstriction, f2e9b199-969f-453c-8714-fa85c89a191a, mf.ievrtrustedvideoplugin_setconstriction
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEVRTrustedVideoPlugin::SetConstriction
 - evr/IEVRTrustedVideoPlugin::SetConstriction
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IEVRTrustedVideoPlugin.SetConstriction
archived: true
---

# IEVRTrustedVideoPlugin::SetConstriction


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Limits the effective video resolution.

## -parameters

### -param dwKPix [in]

Maximum number of source pixels that may appear in the final video image, in thousands of pixels. If the value is zero, the video is disabled. If the value is MAXDWORD (0xFFFFFFFF), video constriction is removed and the video may be rendered at full resolution.

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
</table>

## -remarks

This method limits the effective resolution of the video image. The actual resolution on the target device might be higher, due to stretching the image.

The EVR might call this method at any time if the <a href="/windows/desktop/api/evr/nf-evr-ievrtrustedvideoplugin-canconstrict">IEVRTrustedVideoPlugin::CanConstrict</a> method returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>