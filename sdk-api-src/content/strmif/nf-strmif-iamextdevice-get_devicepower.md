---
UID: NF:strmif.IAMExtDevice.get_DevicePower
title: IAMExtDevice::get_DevicePower (strmif.h)
description: The get_DevicePower method retrieves the external device's power mode.
helpviewer_keywords: ["IAMExtDevice interface [DirectShow]","get_DevicePower method","IAMExtDevice.get_DevicePower","IAMExtDevice::get_DevicePower","IAMExtDeviceget_DevicePower","dshow.iamextdevice_get_devicepower","get_DevicePower","get_DevicePower method [DirectShow]","get_DevicePower method [DirectShow]","IAMExtDevice interface","strmif/IAMExtDevice::get_DevicePower"]
old-location: dshow\iamextdevice_get_devicepower.htm
tech.root: dshow
ms.assetid: 7f25aac8-13ad-4ea2-96df-351da4729666
ms.date: 4/26/2023
ms.keywords: IAMExtDevice interface [DirectShow],get_DevicePower method, IAMExtDevice.get_DevicePower, IAMExtDevice::get_DevicePower, IAMExtDeviceget_DevicePower, dshow.iamextdevice_get_devicepower, get_DevicePower, get_DevicePower method [DirectShow], get_DevicePower method [DirectShow],IAMExtDevice interface, strmif/IAMExtDevice::get_DevicePower
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
 - IAMExtDevice::get_DevicePower
 - strmif/IAMExtDevice::get_DevicePower
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
 - IAMExtDevice.get_DevicePower
---

# IAMExtDevice::get_DevicePower


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_DevicePower</code> method retrieves the external device's power mode.

## -parameters

### -param pPowerMode [out]

Pointer to a <b>long</b> integer that receives one of the following values, indicating the device's power mode.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_POWER_OFF</td>
<td>Power is off.</td>
</tr>
<tr>
<td>ED_POWER_ON</td>
<td>Power if on.</td>
</tr>
<tr>
<td>ED_POWER_STANDBY</td>
<td>Device is in standby mode.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

In Windows XP Service Pack 2 and later, the following additional power mode is defined.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ED_POWER_DEVICE_DEPENDENT</td>
<td>Power is on with limited functions.</td>
</tr>
</table>
 

To use this constant, include the header file Xprtdefs.h.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>
The <a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> and UVC drivers return ED_POWER_ON when the camcorder is on. If the camcorder is off or in standby mode, the DV driver is not loaded, so this method is not available. If the camcorder is removed unexpectedly, the method can return ERROR_GEN_FAILURE.


<a href="/windows/desktop/DirectShow/mstape-driver">MSTape</a> supports both ED_POWER_OFF and ED_POWER_ON, but not ED_POWER_STANDBY.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamextdevice">IAMExtDevice Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamextdevice-put_devicepower">IAMExtDevice::put_DevicePower</a>