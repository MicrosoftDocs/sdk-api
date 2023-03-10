---
UID: NF:imapi2.IDiscRecorder2Ex.SendCommandSendDataToDevice
title: IDiscRecorder2Ex::SendCommandSendDataToDevice (imapi2.h)
description: Sends a MMC command and its associated data buffer to the recording device.
helpviewer_keywords: ["IDiscRecorder2Ex interface [IMAPI]","SendCommandSendDataToDevice method","IDiscRecorder2Ex.SendCommandSendDataToDevice","IDiscRecorder2Ex::SendCommandSendDataToDevice","SendCommandSendDataToDevice","SendCommandSendDataToDevice method [IMAPI]","SendCommandSendDataToDevice method [IMAPI]","IDiscRecorder2Ex interface","imapi.idiscrecorder2ex_sendcommandsenddatatodevice","imapi2/IDiscRecorder2Ex::SendCommandSendDataToDevice"]
old-location: imapi\idiscrecorder2ex_sendcommandsenddatatodevice.htm
tech.root: imapi
ms.assetid: e893c3d8-1bf8-461e-9792-3b7d6d3beebb
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2Ex interface [IMAPI],SendCommandSendDataToDevice method, IDiscRecorder2Ex.SendCommandSendDataToDevice, IDiscRecorder2Ex::SendCommandSendDataToDevice, SendCommandSendDataToDevice, SendCommandSendDataToDevice method [IMAPI], SendCommandSendDataToDevice method [IMAPI],IDiscRecorder2Ex interface, imapi.idiscrecorder2ex_sendcommandsenddatatodevice, imapi2/IDiscRecorder2Ex::SendCommandSendDataToDevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder2Ex::SendCommandSendDataToDevice
 - imapi2/IDiscRecorder2Ex::SendCommandSendDataToDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2Ex.SendCommandSendDataToDevice
---

# IDiscRecorder2Ex::SendCommandSendDataToDevice


## -description

Sends a MMC command and its associated data buffer to the recording device.

## -parameters

### -param Cdb [in]

Command packet to send to the device.

### -param CdbSize [in]

Size, in bytes, of the command packet to send. Must be between 6 and 16 bytes.

### -param SenseBuffer [out]

Sense data returned by the recording device.

### -param Timeout [in]

Time limit, in seconds, allowed for the send command to receive a result.

### -param Buffer [in]

Buffer containing data associated with the send command. Must not be <b>NULL</b>.

### -param BufferSize [in]

Size, in bytes, of the data buffer to send. Must not be zero.

## -returns

S_OK or one of the following values can be returned on success, but other success codes may be returned as a result of implementation:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_IMAPI_COMMAND_HAS_SENSE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The device fails the command, but returns sense data.

Value: 0x00AA0200

</td>
</tr>
</table>
 

The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_IMAPI_RECORDER_GET_CONFIGURATION_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The drive does not support the GET CONFIGURATION command.

Value: 0xC0AA020C

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_NO_SUCH_FEATURE</b></dt>
</dl>
</td>
<td width="60%">
The feature page requested is not supported by the device.

Value: 0xC0AA020A

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
<dt><b>E_IMAPI_RECORDER_FEATURE_IS_NOT_CURRENT</b></dt>
</dl>
</td>
<td width="60%">
The feature page requested is supported, but is not marked as current.

Value: 0xC0AA020B

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
</table>

## -remarks

For details of the contents of the command packet, sense data, and input data buffer, see the latest revision of the MMC specification at ftp://ftp.t10.org/t10/drafts/mmc5.

Client-defined commands (CDBs) used with this method must be between 6 and 16 bytes in length. In addition, the size of each command must match the size defined by the operation code as defined in the following table.

<table>
<tr>
<th>CDB operation code range</th>
<th>CDB group</th>
<th>Required CDB size</th>
</tr>
<tr>
<td>0x00 — 0x1F</td>
<td>0</td>
<td>6 bytes</td>
</tr>
<tr>
<td>0x20 — 0x3F</td>
<td>1</td>
<td>10 bytes</td>
</tr>
<tr>
<td>0x40 — 0x5F</td>
<td>2</td>
<td>10 bytes</td>
</tr>
<tr>
<td>0x60 — 0x7F</td>
<td>3</td>
<td>Will enforce standard-specified size requirements for this opcode range in the future.</td>
</tr>
<tr>
<td>0x80 — 0x9F</td>
<td>4</td>
<td>16 bytes</td>
</tr>
<tr>
<td>0xA0 — 0xBF</td>
<td>5</td>
<td>12 bytes</td>
</tr>
<tr>
<td>0xC0 — 0xDF</td>
<td>6</td>
<td>Vendor Unique - Any size allowed</td>
</tr>
<tr>
<td>0xE0 — 0xFF</td>
<td>7</td>
<td>Vendor Unique - Any size allowed</td>
</tr>
</table>
 

Some very early devices used vendor-unique opcodes and therefore some opcodes cannot be validated in this manner. The following opcodes are still valid and only verify that the size is between 6 and 16 bytes:



0x02, 0x05, 0x06, 0x09, 0x0C, 0x0D, 0x0E, 0x0F, 0x10, 0x13, 0x14, 0x19, 0x20, 0x21, 0x22, 0x23, 0x24, 0x26, 0x27, 0x29, 0x2C, 0x2D

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex">IDiscRecorder2Ex</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandgetdatafromdevice">IDiscRecorder2Ex::SendCommandGetDataFromDevice</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscrecorder2ex-sendcommandnodata">IDiscRecorder2Ex::SendCommandNoData</a>