---
UID: NF:strmif.IAMExtDevice.Calibrate
title: IAMExtDevice::Calibrate
author: windows-sdk-content
description: The Calibrate method calibrates an external device's transport mechanism.
old-location: dshow\iamextdevice_calibrate.htm
tech.root: DirectShow
ms.assetid: 0c760669-c494-45bb-994e-5b4599db7de4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: Calibrate, Calibrate method [DirectShow], Calibrate method [DirectShow],IAMExtDevice interface, IAMExtDevice interface [DirectShow],Calibrate method, IAMExtDevice.Calibrate, IAMExtDevice::Calibrate, IAMExtDeviceCalibrate, dshow.iamextdevice_calibrate, strmif/IAMExtDevice::Calibrate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtDevice::Calibrate


## -description



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

Filters for various external devices can implement this method differently, depending on the calibration that the device needs. This method assumes the <a href="https://msdn.microsoft.com/50aa04b4-9a04-4d0d-a558-42595a69aef7">IMediaEventSink</a> interface has already established an event sink, or that another event signaling method has been established.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>
The <a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> and UVC drivers do not support this method. The method returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0423e888-39d1-45cb-9bcf-722240a31fbd">IAMExtDevice Interface</a>
 

 

