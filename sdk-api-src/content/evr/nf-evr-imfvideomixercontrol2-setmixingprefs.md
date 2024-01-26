---
UID: NF:evr.IMFVideoMixerControl2.SetMixingPrefs
title: IMFVideoMixerControl2::SetMixingPrefs (evr.h)
description: Sets the preferences for video deinterlacing.
helpviewer_keywords: ["IMFVideoMixerControl2 interface [Media Foundation]","SetMixingPrefs method","IMFVideoMixerControl2.SetMixingPrefs","IMFVideoMixerControl2::SetMixingPrefs","SetMixingPrefs","SetMixingPrefs method [Media Foundation]","SetMixingPrefs method [Media Foundation]","IMFVideoMixerControl2 interface","evr/IMFVideoMixerControl2::SetMixingPrefs","mf.imfvideomixercontrol2_setmixingprefs"]
old-location: mf\imfvideomixercontrol2_setmixingprefs.htm
tech.root: mfarchive
ms.assetid: ae8fa85a-bdae-4fbf-b9d4-a987eb1c4c41
ms.date: 12/05/2018
ms.keywords: IMFVideoMixerControl2 interface [Media Foundation],SetMixingPrefs method, IMFVideoMixerControl2.SetMixingPrefs, IMFVideoMixerControl2::SetMixingPrefs, SetMixingPrefs, SetMixingPrefs method [Media Foundation], SetMixingPrefs method [Media Foundation],IMFVideoMixerControl2 interface, evr/IMFVideoMixerControl2::SetMixingPrefs, mf.imfvideomixercontrol2_setmixingprefs
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
 - IMFVideoMixerControl2::SetMixingPrefs
 - evr/IMFVideoMixerControl2::SetMixingPrefs
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
 - IMFVideoMixerControl2.SetMixingPrefs
archived: true
---

# IMFVideoMixerControl2::SetMixingPrefs


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the preferences for video deinterlacing.

## -parameters

### -param dwMixFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/evr/ne-evr-mfvideomixprefs">MFVideoMixPrefs</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2">IMFVideoMixerControl2</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>