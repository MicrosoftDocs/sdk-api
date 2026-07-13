---
UID: NF:evr.IMFVideoMixerControl2.GetMixingPrefs
title: IMFVideoMixerControl2::GetMixingPrefs (evr.h)
description: Gets the current preferences for video deinterlacing.
helpviewer_keywords: ["GetMixingPrefs","GetMixingPrefs method [Media Foundation]","GetMixingPrefs method [Media Foundation]","IMFVideoMixerControl2 interface","IMFVideoMixerControl2 interface [Media Foundation]","GetMixingPrefs method","IMFVideoMixerControl2.GetMixingPrefs","IMFVideoMixerControl2::GetMixingPrefs","evr/IMFVideoMixerControl2::GetMixingPrefs","mf.imfvideomixercontrol2_getmixingprefs"]
old-location: mf\imfvideomixercontrol2_getmixingprefs.htm
tech.root: mfarchive
ms.assetid: 4ec03db2-9e7f-4a11-8d69-7654391a33d8
ms.date: 12/05/2018
ms.keywords: GetMixingPrefs, GetMixingPrefs method [Media Foundation], GetMixingPrefs method [Media Foundation],IMFVideoMixerControl2 interface, IMFVideoMixerControl2 interface [Media Foundation],GetMixingPrefs method, IMFVideoMixerControl2.GetMixingPrefs, IMFVideoMixerControl2::GetMixingPrefs, evr/IMFVideoMixerControl2::GetMixingPrefs, mf.imfvideomixercontrol2_getmixingprefs
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoMixerControl2::GetMixingPrefs
 - evr/IMFVideoMixerControl2::GetMixingPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IMFVideoMixerControl2.GetMixingPrefs
archived: true
---

# IMFVideoMixerControl2::GetMixingPrefs


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Gets the current preferences for video deinterlacing.

## -parameters

### -param pdwMixFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/evr/ne-evr-mfvideomixprefs">MFVideoMixPrefs</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2">IMFVideoMixerControl2</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>