---
UID: NF:vidcap.ICameraControl.put_Tilt
title: ICameraControl::put_Tilt (vidcap.h)
description: The put_Tilt method sets the camera's tilt angle.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Tilt method","ICameraControl.put_Tilt","ICameraControl::put_Tilt","ICameraControlput_Tilt","dshow.icameracontrol_put_tilt","put_Tilt","put_Tilt method [DirectShow]","put_Tilt method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Tilt"]
old-location: dshow\icameracontrol_put_tilt.htm
tech.root: dshow
ms.assetid: e75adedb-5cf2-4b2c-bb57-1bfedfc81979
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_Tilt method, ICameraControl.put_Tilt, ICameraControl::put_Tilt, ICameraControlput_Tilt, dshow.icameracontrol_put_tilt, put_Tilt, put_Tilt method [DirectShow], put_Tilt method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Tilt
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
 - ICameraControl::put_Tilt
 - vidcap/ICameraControl::put_Tilt
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
 - ICameraControl.put_Tilt
---

# ICameraControl::put_Tilt


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Tilt</code> method sets the camera's tilt angle.

## -parameters

### -param Value [in]

Specifies the tilt angle, in degrees. Positive values point the camera up, and negative values point the camera down. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tilt">ICameraControl::getRange_Tilt</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>