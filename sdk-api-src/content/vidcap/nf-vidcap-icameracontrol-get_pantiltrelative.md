---
UID: NF:vidcap.ICameraControl.get_PanTiltRelative
title: ICameraControl::get_PanTiltRelative (vidcap.h)
description: The get_PanTiltRelative method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_PanTiltRelative method","ICameraControl.get_PanTiltRelative","ICameraControl::get_PanTiltRelative","ICameraControlget_PanTiltRelative","dshow.icameracontrol_get_pantiltrelative","get_PanTiltRelative","get_PanTiltRelative method [DirectShow]","get_PanTiltRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_PanTiltRelative"]
old-location: dshow\icameracontrol_get_pantiltrelative.htm
tech.root: dshow
ms.assetid: 5d96dcfb-c0c4-4521-bf1f-30947577d305
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_PanTiltRelative method, ICameraControl.get_PanTiltRelative, ICameraControl::get_PanTiltRelative, ICameraControlget_PanTiltRelative, dshow.icameracontrol_get_pantiltrelative, get_PanTiltRelative, get_PanTiltRelative method [DirectShow], get_PanTiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanTiltRelative
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - ICameraControl::get_PanTiltRelative
 - vidcap/ICameraControl::get_PanTiltRelative
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
 - ICameraControl.get_PanTiltRelative
---

# ICameraControl::get_PanTiltRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_PanTiltRelative</code> method returns the camera's relative pan and tilt. The relative pan and tilt are expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pPanValue [out]

Receives the relative pan. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_panrelative">ICameraControl::get_PanRelative</a>.

### -param pTiltValue [out]

Receives the relative tilt. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-get_tiltrelative">ICameraControl::get_TiltRelative</a>.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>