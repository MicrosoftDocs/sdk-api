---
UID: NF:vidcap.ICameraControl.put_PanTilt
title: ICameraControl::put_PanTilt (vidcap.h)
description: The put_PanTilt method sets the camera's pan and tilt angles.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_PanTilt method","ICameraControl.put_PanTilt","ICameraControl::put_PanTilt","ICameraControlput_PanTilt","dshow.icameracontrol_put_pantilt","put_PanTilt","put_PanTilt method [DirectShow]","put_PanTilt method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_PanTilt"]
old-location: dshow\icameracontrol_put_pantilt.htm
tech.root: dshow
ms.assetid: d9aa052a-72f9-4a17-bebe-809f43264481
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_PanTilt method, ICameraControl.put_PanTilt, ICameraControl::put_PanTilt, ICameraControlput_PanTilt, dshow.icameracontrol_put_pantilt, put_PanTilt, put_PanTilt method [DirectShow], put_PanTilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PanTilt
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
 - ICameraControl::put_PanTilt
 - vidcap/ICameraControl::put_PanTilt
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
 - ICameraControl.put_PanTilt
---

# ICameraControl::put_PanTilt


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_PanTilt</code> method sets the camera's pan and tilt angles.

## -parameters

### -param PanValue [in]

Specifies the panning angle, in arc seconds. An arc second is 1/3600th of a degree. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_pan">ICameraControl::put_Pan</a>.

### -param TiltValue [in]

Specifies the tilt angle, in arc seconds. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-put_tilt">ICameraControl::put_Tilt</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>