---
UID: NF:evr.IEVRTrustedVideoPlugin.CanConstrict
title: IEVRTrustedVideoPlugin::CanConstrict (evr.h)
description: Queries whether the plug-in can limit the effective video resolution.
helpviewer_keywords: ["16bb31c3-51f7-4d9b-946c-f366fb6e5dee","CanConstrict","CanConstrict method [Media Foundation]","CanConstrict method [Media Foundation]","IEVRTrustedVideoPlugin interface","IEVRTrustedVideoPlugin interface [Media Foundation]","CanConstrict method","IEVRTrustedVideoPlugin.CanConstrict","IEVRTrustedVideoPlugin::CanConstrict","evr/IEVRTrustedVideoPlugin::CanConstrict","mf.ievrtrustedvideoplugin_canconstrict"]
old-location: mf\ievrtrustedvideoplugin_canconstrict.htm
tech.root: mfarchive
ms.assetid: 16bb31c3-51f7-4d9b-946c-f366fb6e5dee
ms.date: 12/05/2018
ms.keywords: 16bb31c3-51f7-4d9b-946c-f366fb6e5dee, CanConstrict, CanConstrict method [Media Foundation], CanConstrict method [Media Foundation],IEVRTrustedVideoPlugin interface, IEVRTrustedVideoPlugin interface [Media Foundation],CanConstrict method, IEVRTrustedVideoPlugin.CanConstrict, IEVRTrustedVideoPlugin::CanConstrict, evr/IEVRTrustedVideoPlugin::CanConstrict, mf.ievrtrustedvideoplugin_canconstrict
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
 - IEVRTrustedVideoPlugin::CanConstrict
 - evr/IEVRTrustedVideoPlugin::CanConstrict
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
 - IEVRTrustedVideoPlugin.CanConstrict
archived: true
---

# IEVRTrustedVideoPlugin::CanConstrict


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Queries whether the plug-in can limit the effective video resolution.

## -parameters

### -param pYes [out]

Receives a Boolean value. If <b>TRUE</b>, the plug-in can limit the effective video resolution. Otherwise, the plug-in cannot limit the video resolution. If the method fails, the EVR treats the value as <b>FALSE</b> (not supported).

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

Constriction is a protection mechanism that limits the effective resolution of the video frame to a specified maximum number of pixels.

Video constriction can be implemented by either the mixer or the presenter.

If the method returns <b>TRUE</b>, the EVR might call <a href="/windows/desktop/api/evr/nf-evr-ievrtrustedvideoplugin-setconstriction">IEVRTrustedVideoPlugin::SetConstriction</a> at any time.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin">IEVRTrustedVideoPlugin</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>