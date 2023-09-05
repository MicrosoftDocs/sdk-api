---
UID: NF:strmif.IAMExtDevice.Calibrate
title: IAMExtDevice::Calibrate (strmif.h)
description: The Calibrate method calibrates an external device's transport mechanism.
helpviewer_keywords: ["Calibrate","Calibrate method [DirectShow]","Calibrate method [DirectShow]","IAMExtDevice interface","IAMExtDevice interface [DirectShow]","Calibrate method","IAMExtDevice.Calibrate","IAMExtDevice::Calibrate","IAMExtDeviceCalibrate","dshow.iamextdevice_calibrate","strmif/IAMExtDevice::Calibrate"]
old-location: dshow\iamextdevice_calibrate.htm
tech.root: dshow
ms.assetid: 0c760669-c494-45bb-994e-5b4599db7de4
ms.date: 4/26/2023
ms.keywords: Calibrate, Calibrate method [DirectShow], Calibrate method [DirectShow],IAMExtDevice interface, IAMExtDevice interface [DirectShow],Calibrate method, IAMExtDevice.Calibrate, IAMExtDevice::Calibrate, IAMExtDeviceCalibrate, dshow.iamextdevice_calibrate, strmif/IAMExtDevice::Calibrate
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMExtDevice::Calibrate
 - strmif/IAMExtDevice::Calibrate
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
 - IAMExtDevice.Calibrate
---

# IAMExtDevice::Calibrate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Calibrate</code> method calibrates an external device's transport mechanism.



This method is not implemented.

## -parameters

### -param hEvent [in]

Handle to an event. The event is signaled when the action is complete.

### -param Mode [in]

Specifies a value that activates or deactivates the calibration process:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_ACTIVE</td>
<td>Activates the calibration process.</td>
</tr>
<tr>
<td>ED_INACTIVE</td>
<td>Deactivates the calibration process.</td>
</tr>
<tr>
<td><b>NULL</b></td>
<td>No action; return the calibration status in <i>pStatus</i>.</td>
</tr>
</table>

### -param pStatus [out]

Pointer to a <b>long</b> integer that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Calibration is active.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Calibration is inactive.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

Use this method on certain external devices that require calibration; for example, rewinding a tape and resetting the counter, or computing the frame offset for a timecode reader.

Filters for various external devices can implement this method differently, depending on the calibration that the device needs. This method assumes the <a href="/windows/desktop/api/strmif/nn-strmif-imediaeventsink">IMediaEventSink</a> interface has already established an event sink, or that another event signaling method has been established.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>
The <a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> and UVC drivers do not support this method. The method returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>