---
UID: NF:vidcap.ICameraControl.put_Roll
title: ICameraControl::put_Roll (vidcap.h)
description: The put_Roll method sets the camera's roll angle.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_Roll method","ICameraControl.put_Roll","ICameraControl::put_Roll","ICameraControlput_Roll","dshow.icameracontrol_put_roll","put_Roll","put_Roll method [DirectShow]","put_Roll method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_Roll"]
old-location: dshow\icameracontrol_put_roll.htm
tech.root: dshow
ms.assetid: f74c7acc-e141-4238-bcbe-7890646e706c
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_Roll method, ICameraControl.put_Roll, ICameraControl::put_Roll, ICameraControlput_Roll, dshow.icameracontrol_put_roll, put_Roll, put_Roll method [DirectShow], put_Roll method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Roll
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
 - ICameraControl::put_Roll
 - vidcap/ICameraControl::put_Roll
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
 - ICameraControl.put_Roll
---

# ICameraControl::put_Roll


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Roll</code> method sets the camera's roll angle.

## -parameters

### -param Value [in]

Specifies the roll angle, in degrees. Positive values are clockwise along the image viewing axis, and negative values are counter clockwise. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_roll">ICameraControl::getRange_Roll</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>