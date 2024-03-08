---
UID: NF:vidcap.ICameraControl.getRange_IrisRelative
title: ICameraControl::getRange_IrisRelative (vidcap.h)
description: The getRange_IrisRelative method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","getRange_IrisRelative method","ICameraControl.getRange_IrisRelative","ICameraControl::getRange_IrisRelative","ICameraControlgetRange_IrisRelative","dshow.icameracontrol_getrange_irisrelative","getRange_IrisRelative","getRange_IrisRelative method [DirectShow]","getRange_IrisRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::getRange_IrisRelative"]
old-location: dshow\icameracontrol_getrange_irisrelative.htm
tech.root: dshow
ms.assetid: 9816e29b-3366-49e7-aa4c-46b06963c176
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],getRange_IrisRelative method, ICameraControl.getRange_IrisRelative, ICameraControl::getRange_IrisRelative, ICameraControlgetRange_IrisRelative, dshow.icameracontrol_getrange_irisrelative, getRange_IrisRelative, getRange_IrisRelative method [DirectShow], getRange_IrisRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::getRange_IrisRelative
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
 - ICameraControl::getRange_IrisRelative
 - vidcap/ICameraControl::getRange_IrisRelative
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
 - ICameraControl.getRange_IrisRelative
---

# ICameraControl::getRange_IrisRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_IrisRelative</code> method returns the range of relative aperture settings supported by the camera. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pMin [out]

Receives the minimum relative aperture setting.

### -param pMax [out]

Receives the maximum relative aperture setting.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default relative aperture setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>