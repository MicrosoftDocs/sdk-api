---
UID: NF:vidcap.ICameraControl.put_ExposureRelative
title: ICameraControl::put_ExposureRelative (vidcap.h)
description: The put_ExposureRelative method sets the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_ExposureRelative method","ICameraControl.put_ExposureRelative","ICameraControl::put_ExposureRelative","ICameraControlput_ExposureRelative","dshow.icameracontrol_put_exposurerelative","put_ExposureRelative","put_ExposureRelative method [DirectShow]","put_ExposureRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_ExposureRelative"]
old-location: dshow\icameracontrol_put_exposurerelative.htm
tech.root: dshow
ms.assetid: 4afc3f7f-bba2-4160-b917-c792467d6305
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_ExposureRelative method, ICameraControl.put_ExposureRelative, ICameraControl::put_ExposureRelative, ICameraControlput_ExposureRelative, dshow.icameracontrol_put_exposurerelative, put_ExposureRelative, put_ExposureRelative method [DirectShow], put_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_ExposureRelative
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
 - ICameraControl::put_ExposureRelative
 - vidcap/ICameraControl::put_ExposureRelative
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
 - ICameraControl.put_ExposureRelative
---

# ICameraControl::put_ExposureRelative


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_ExposureRelative</code> method sets the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param Value [in]

Specifies the relative exposure. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_exposurerelative">ICameraControl::getRange_ExposureRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Set the exposure to the default exposure time, which is implementation dependent.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Increment the exposure time by one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Decrement the exposure time by one step.</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>