---
UID: NF:imapi2.IDiscFormat2RawCD.SetWriteSpeed
title: IDiscFormat2RawCD::SetWriteSpeed (imapi2.h)
author: windows-sdk-content
description: Sets the write speed of the disc recorder.
old-location: imapi\idiscformat2rawcd_setwritespeed.htm
tech.root: imapi
ms.assetid: 93021007-6ed8-4322-93bb-c52796a4ab66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],SetWriteSpeed method, IDiscFormat2RawCD.SetWriteSpeed, IDiscFormat2RawCD::SetWriteSpeed, SetWriteSpeed, SetWriteSpeed method [IMAPI], SetWriteSpeed method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_setwritespeed, imapi2/IDiscFormat2RawCD::SetWriteSpeed
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2RawCD.SetWriteSpeed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2RawCD::SetWriteSpeed


## -description


Sets the write speed of the disc recorder. 


## -parameters




### -param RequestedSectorsPerSecond [in]

Requested write speed measured in disc sectors per second.

A value of 0xFFFFFFFF (-1) requests that the write occurs using the fastest supported speed for the media.  This is the default.


### -param RotationTypeIsPureCAV [in]

Requested rotational-speed control type. Set to VARIANT_TRUE to request constant angular velocity (CAV)  rotational-speed control type. Set to VARIANT_FALSE to use another rotational-speed control type that the recorder supports. The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The request requires a current disc recorder to be selected.

Value: 0xC0AA0003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_COMMAND_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The device failed to accept the command within the timeout period. This may be caused by the device having entered an inconsistent state, or the timeout value for the command may need to be increased.

Value: 0xC0AA020D

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_INVALID_RESPONSE_FROM_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The device reported unexpected or invalid data for a command.

Value: 0xC0AA02FF

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_UPSIDE_DOWN</b></dt>
</dl>
</td>
<td width="60%">
The media is inserted upside down.

Value: 0xC0AA0204

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_BECOMING_READY</b></dt>
</dl>
</td>
<td width="60%">
The drive reported that it is in the process of becoming ready. Please try the request again later.

Value: 0xC0AA0205

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
There is no media in the device.

Value: 0xC0AA0202

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_FORMAT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The media is currently being formatted. Please wait for the format to complete before attempting to use the media.

Value: 0xC0AA0206

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The drive reported that it is performing a long-running operation, such as finishing a write. The drive may be unusable for a long period of time.

Value: 0xC0AA0207

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_LOSS_OF_STREAMING</b></dt>
</dl>
</td>
<td width="60%">
The write failed because the drive did not receive data quickly enough to continue writing. Moving the source data to the local computer, reducing the write speed, or enabling a "buffer underrun free" setting may resolve this issue.

Value: 0xC0AA0300

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
The media is not compatible or of unknown physical format.

Value: 0xC0AA0203

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_DVD_STRUCTURE_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The DVD structure is not present. This may be caused by incompatible drive/medium used.

Value: 0xC0AA020E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_NO_SUCH_MODE_PAGE</b></dt>
</dl>
</td>
<td width="60%">
The device reported that the requested mode page (and type) is not present.

Value: 0xC0AA0201

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_INVALID_MODE_PARAMETERS</b></dt>
</dl>
</td>
<td width="60%">
The drive reported that the combination of parameters provided in the mode page for a MODE SELECT command were not supported.

Value: 0xC0AA0208

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_WRITE_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
The drive reported that the media is write protected.

Value: 0xC0AA0209

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_SPEED_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The media's speed is incompatible with the device. This may be caused by using higher or lower speed media than the range of speeds supported by the device.

Value: 0xC0AA020F

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

Value: 6

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_DEV_NOT_EXIST)</b></dt>
</dl>
</td>
<td width="60%">
The specified network resource or device is no longer available.

Value: 55

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_LOCKED</b></dt>
</dl>
</td>
<td width="60%">
The device associated with this recorder during the last operation has been exclusively locked, causing this operation to failed.

Value: 0xC0AA0210

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Only blank CD-R/RW media is supported.

Value: 0xC0AA0606

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_BLANK</b></dt>
</dl>
</td>
<td width="60%">
Only blank CD-R/RW media is supported.

Value: 0xC0AA0607

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_CLIENT_NAME_IS_NOT_VALID</b></dt>
</dl>
</td>
<td width="60%">
The client name is not valid.

Value: 0xC0AA0604

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_IMAPI_ROTATIONADJUSTED</b></dt>
</dl>
</td>
<td width="60%">
The requested rotation type was not supported by the drive and the rotation type was adjusted.

Value: 0x00AA0005

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_IMAPI_SPEEDADJUSTED</b></dt>
</dl>
</td>
<td width="60%">
The requested write speed was not supported by the drive and the speed was adjusted.

Value: 0x00AA0004

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_IMAPI_BOTHADJUSTED</b></dt>
</dl>
</td>
<td width="60%">
The requested write speed and rotation type were not supported by the drive and they were both adjusted.

Value: 0x00AA0006

</td>
</tr>
</table>
 




## -remarks



This method sets the write speed and type of rotational-speed control for a recorder. Requested values might differ from the values set in the recorder. To specify the recorder, call the <a href="https://msdn.microsoft.com/d3deefa8-40be-4cdc-aae1-e5fbe508f16f">IDiscFormat2RawCD::put_Recorder</a> method. 

If the recorder supports the requested write speed,  the disc device uses the requested value. If the recorder does not support the requested write speed,  the recorder uses a write speed that it does support that is closest to the requested value. The <a href="https://msdn.microsoft.com/f369f719-7db6-4a79-a5fa-d174bf12acbc">IDiscFormat2RawCD::get_CurrentWriteSpeed</a> property contains the value used by the recorder.

To retrieve a list of the write speeds that the recorder and current media supports, call the <a href="https://msdn.microsoft.com/7ebcc42f-d864-407f-a1a6-d4811ca8221c">IDiscFormat2RawCD::get_SupportedWriteSpeeds</a> method.

If you request constant angular velocity (CAV) for rotational-speed control type and the recorder does not support CAV,  the disc device uses another type of rotational-speed control type that it supports. The <a href="https://msdn.microsoft.com/ca3ab4e3-e87c-4081-bb65-c1d8c3f1ff37">IDiscFormat2RawCD::get_CurrentRotationTypeIsPureCAV</a> property indicates the value used by the recorder.

To retrieve the requested values, call the <a href="https://msdn.microsoft.com/0b718fe5-197e-4dc7-a8df-f2febf76aaab">IDiscFormat2RawCD::get_RequestedWriteSpeed</a> and <a href="https://msdn.microsoft.com/884624e2-96d7-491a-add3-a5bd3edc473e">IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



<a href="https://msdn.microsoft.com/ca3ab4e3-e87c-4081-bb65-c1d8c3f1ff37">IDiscFormat2RawCD::get_CurrentRotationTypeIsPureCAV</a>



<a href="https://msdn.microsoft.com/884624e2-96d7-491a-add3-a5bd3edc473e">IDiscFormat2RawCD::get_RequestedRotationTypeIsPureCAV</a>



<a href="https://msdn.microsoft.com/00a7c10a-7790-4193-928c-d3211047dbbe">IDiscFormat2RawCD::get_SupportedWriteSpeedDescriptors</a>



<a href="https://msdn.microsoft.com/7ebcc42f-d864-407f-a1a6-d4811ca8221c">IDiscFormat2RawCD::get_SupportedWriteSpeeds</a>
 

 

