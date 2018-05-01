---
UID: NS:winbio_ioctl._WINBIO_CAPTURE_DATA
title: "_WINBIO_CAPTURE_DATA"
author: windows-driver-content
description: The IOCTL_BIOMETRIC_CAPTURE_DATA IOCTL returns the WINBIO_CAPTURE_DATA structure as output.
old-location: biometric\winbio_capture_data.htm
old-project: biometric
ms.assetid: 1d1df123-4c1a-498b-b629-ca63336a762b
ms.author: windowsdriverdev
ms.date: 2/20/2018
ms.keywords: "*PWINBIO_CAPTURE_DATA, PWINBIO_CAPTURE_DATA, PWINBIO_CAPTURE_DATA structure pointer [Biometric Devices], WINBIO_CAPTURE_DATA, WINBIO_CAPTURE_DATA structure [Biometric Devices], _WINBIO_CAPTURE_DATA, biometric.winbio_capture_data, biometric_ref_be8dfe0a-ed13-4b31-af93-8fde60a1640f.xml, winbio_ioctl/PWINBIO_CAPTURE_DATA, winbio_ioctl/WINBIO_CAPTURE_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_ioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_CAPTURE_DATA, *PWINBIO_CAPTURE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winbio_ioctl.h
api_name:
-	WINBIO_CAPTURE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_CAPTURE_DATA structure


## -description


The <a href="https://msdn.microsoft.com/library/windows/hardware/ff536429">IOCTL_BIOMETRIC_CAPTURE_DATA</a> IOCTL returns the WINBIO_CAPTURE_DATA structure as output.


## -struct-fields




### -field PayloadSize

 The total size of the payload.  This includes the fixed length structure and any variable data at the end.


### -field WinBioHresult

The status detail of the I/O operation.  This is where WINBIO error and information codes will be passed. The following table shows possible values for this member.

<table>
<tr>
<th>Status value</th>
<th>Description</th>
</tr>
<tr>
<td>
S_OK

</td>
<td>
The operation completed successfully.

</td>
</tr>
<tr>
<td>
WINBIO_E_DATA_COLLECTION_IN_PROGRESS

</td>
<td>
There is already a data collection IOCTL pending.

</td>
</tr>
<tr>
<td>
WINBIO_E_UNSUPPORTED_DATA_FORMAT

</td>
<td>
The format specified is not supported by this driver and device.

</td>
</tr>
<tr>
<td>
WINBIO_E_UNSUPPORTED_DATA_TYPE

</td>
<td>
The type of data requested is not supported by this driver and device.

</td>
</tr>
<tr>
<td>
WINBIO_E_INVALID_DEVICE_STATE

</td>
<td>
The device could not be put into biometric capture mode.  This could be because the device is in another non-data collection mode.

</td>
</tr>
<tr>
<td>
HRESULT_FROM_NT(STATUS_IO_DEVICE_ERROR)

</td>
<td>
The operation was not completed due to device error.

</td>
</tr>
<tr>
<td>
WINBIO_E_DEVICE_BUSY

</td>
<td>
The device is in the middle of a vendor-specific operation.

</td>
</tr>
<tr>
<td>
WINBIO_E_CANCELED

</td>
<td>
The operation was canceled either by the caller, or an IOCTL_BIOMETRIC_RESET request.

</td>
</tr>
<tr>
<td>
WINBIO_E_UNSUPPORTED_PURPOSE

</td>
<td>
The capture purpose specified is not supported by the driver.

</td>
</tr>
</table>
 


### -field SensorStatus

The WINBIO_SENSOR_STATUS status of the sensor after the capture has occurred. It specifies the operating status of the sensor.

WINBIO_SENSOR_STATUS can be queried at any time.  When WINBIO_SENSOR_STATUS is returned upon a capture I/O completion, it indicates whether a capture was successful. Possible values are shown in the following table.

<table>
<tr>
<th>
              
                Sensor status code
              
            </th>
<th>
              
                Description
              
            </th>
</tr>
<tr>
<td>
WINBIO_SENSOR_ACCEPT

</td>
<td>
The sensor just successfully completed a capture operation.  This should only be returned immediately after a capture operation.  The sensor will then return to WINBIO_SENSOR_READY or WINBIO_SENSOR_BUSY.

</td>
</tr>
<tr>
<td>
WINBIO_SENSOR_REJECT

</td>
<td>
The sensor rejected the previous capture operation.  This should only be returned immediately following a capture operation.  The sensor will then return to WINBIO_SENSOR_READY or WINBIO_SENSOR_BUSY.

</td>
</tr>
<tr>
<td>
WINBIO_SENSOR_READY

</td>
<td>
The sensor is ready to capture data.  If there is a pending data capture IOCTL, the sensor is ready to accept data.

</td>
</tr>
<tr>
<td>
WINBIO_SENSOR_BUSY

</td>
<td>
The sensor is busy or in a state where it cannot capture data.  For example, the device could still be initializing after it has been turned on.

</td>
</tr>
<tr>
<td>
WINBIO_SENSOR_NOT_CALIBRATED

</td>
<td>
The sensor must be calibrated before it is put into data collection mode.

</td>
</tr>
<tr>
<td>
WINBIO_SENSOR_FAILURE

</td>
<td>
The sensor device failed.

</td>
</tr>
</table>
 


### -field RejectDetail

If the sensor status was WINBIO_SENSOR_REJECT, this member contains a WINBIO_REJECT_DETAIL value. WINBIO_SENSOR_REJECT specifies the reason a biometric sampling operation failed.

<div class="alert"><b>Important</b>    Values defined for Windows 7 are for fingerprint reject details only.</div>
<div> </div>
Failure detail values for WINBIO_TYPE_FINGERPRINT include:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define WINBIO_FP_TOO_HIGH          ((WINBIO_REJECT_DETAIL)1)
#define WINBIO_FP_TOO_LOW           ((WINBIO_REJECT_DETAIL)2)
#define WINBIO_FP_TOO_LEFT          ((WINBIO_REJECT_DETAIL)3)
#define WINBIO_FP_TOO_RIGHT         ((WINBIO_REJECT_DETAIL)4)
#define WINBIO_FP_TOO_FAST          ((WINBIO_REJECT_DETAIL)5)
#define WINBIO_FP_TOO_SLOW          ((WINBIO_REJECT_DETAIL)6)
#define WINBIO_FP_POOR_QUALITY      ((WINBIO_REJECT_DETAIL)7)
#define WINBIO_FP_TOO_SKEWED        ((WINBIO_REJECT_DETAIL)8)
#define WINBIO_FP_TOO_SHORT         ((WINBIO_REJECT_DETAIL)9)
#define WINBIO_FP_MERGE_FAILURE     ((WINBIO_REJECT_DETAIL)10)</pre>
</td>
</tr>
</table></span></div>

### -field CaptureData

A structure of type <a href="https://msdn.microsoft.com/library/windows/hardware/ff536469">WINBIO_DATA</a> that contains data captured by the device, of the format specified. The <b>Data</b> array member of the WINBIO_DATA structure should contain a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536459">WINBIO_BIR</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536429">IOCTL_BIOMETRIC_CAPTURE_DATA</a>
 

 

