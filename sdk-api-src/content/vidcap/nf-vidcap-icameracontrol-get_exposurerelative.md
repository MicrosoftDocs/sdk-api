---
UID: NF:vidcap.ICameraControl.get_ExposureRelative
title: ICameraControl::get_ExposureRelative (vidcap.h)
description: The get_ExposureRelative method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_ExposureRelative method","ICameraControl.get_ExposureRelative","ICameraControl::get_ExposureRelative","ICameraControlget_ExposureRelative","dshow.icameracontrol_get_exposurerelative","get_ExposureRelative","get_ExposureRelative method [DirectShow]","get_ExposureRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_ExposureRelative"]
old-location: dshow\icameracontrol_get_exposurerelative.htm
tech.root: dshow
ms.assetid: d63cf869-ccb6-45cb-85ba-a1e41faa8086
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_ExposureRelative method, ICameraControl.get_ExposureRelative, ICameraControl::get_ExposureRelative, ICameraControlget_ExposureRelative, dshow.icameracontrol_get_exposurerelative, get_ExposureRelative, get_ExposureRelative method [DirectShow], get_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ExposureRelative
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
 - ICameraControl::get_ExposureRelative
 - vidcap/ICameraControl::get_ExposureRelative
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
 - ICameraControl.get_ExposureRelative
---

# ICameraControl::get_ExposureRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ExposureRelative</code> method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param pValue [out]

Receives the relative exposure. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_exposurerelative">ICameraControl::getRange_ExposureRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Default exposure time.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Incremented by one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Decremented by one step.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>