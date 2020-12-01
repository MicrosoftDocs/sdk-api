---
UID: NF:imapi2.IDiscFormat2RawCD.WriteMedia
title: IDiscFormat2RawCD::WriteMedia (imapi2.h)
description: Writes a DAO-96 raw image to the blank media using MSF 95:00:00 as the starting address.
helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","WriteMedia method","IDiscFormat2RawCD.WriteMedia","IDiscFormat2RawCD::WriteMedia","WriteMedia","WriteMedia method [IMAPI]","WriteMedia method [IMAPI]","IDiscFormat2RawCD interface","imapi.idiscformat2rawcd_writemedia","imapi2/IDiscFormat2RawCD::WriteMedia"]
old-location: imapi\idiscformat2rawcd_writemedia.htm
tech.root: imapi
ms.assetid: 137395f1-b0cf-4bd0-9d3b-a21122eb8b57
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],WriteMedia method, IDiscFormat2RawCD.WriteMedia, IDiscFormat2RawCD::WriteMedia, WriteMedia, WriteMedia method [IMAPI], WriteMedia method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_writemedia, imapi2/IDiscFormat2RawCD::WriteMedia
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
 - IDiscFormat2RawCD::WriteMedia
 - imapi2/IDiscFormat2RawCD::WriteMedia
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
 - IDiscFormat2RawCD.WriteMedia
---

# IDiscFormat2RawCD::WriteMedia


## -description

Writes a DAO-96 raw image to the blank media using MSF 95:00:00 as the starting address.

## -parameters

### -param data [in]

An <b>IStream</b> interface of the data stream to write.

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
<dt><b>E_IMAPI_DF2RAW_STREAM_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provided audio stream is not valid.

Value: 0xC0AA060D

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

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

Value: 0xC0AA0606

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_STREAM_LEADIN_TOO_SHORT</b></dt>
</dl>
</td>
<td width="60%">
The stream does not contain a sufficient number of sectors in the leadin for the current media.

Value: 0xC0AA060F

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
<dt><b>E_IMAPI_DF2RAW_NOT_ENOUGH_SPACE</b></dt>
</dl>
</td>
<td width="60%">
There is not enough space on the media to add the provided session.

Value: 0xC0AA0609

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
<dt><b>E_IMAPI_REQUEST_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The request was canceled.

Value: 0xC0AA0002

</td>
</tr>
</table>

## -remarks

Before calling this method, you must call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_recorder">IDiscFormat2RawCD::put_Recorder</a> and <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-preparemedia">IDiscFormat2RawCD::PrepareMedia</a> methods.

You should also consider calling the following methods if their default values are not appropriate for your application:

<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_bufferunderrunfreedisabled">IDiscFormat2RawCD::put_BufferUnderrunFreeDisabled</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_clientname">IDiscFormat2RawCD::put_ClientName</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_requestedsectortype">IDiscFormat2RawCD::put_RequestedSectorType</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-setwritespeed">IDiscFormat2RawCD::SetWriteSpeed</a>
</li>
</ul>
This method is synchronous. To determine the progress of the write operation, you must implement the <a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents">DDiscFormat2RawCDEvents</a> interface. For examples that show how to implement an event handler in a script, see <a href="/windows/desktop/imapi/monitoring-progress-with-events">Monitoring Progress With Events</a>.

The first sector of the raw image is written at MSF 95:00:00. If your RAW image has a different first sector, please use the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia2">IDiscFormat2RawCD::WriteMedia2</a> method.

This method uses the <b>IStream::Seek</b> method to reach the appropriate starting location in the image for the current media. If the <b>IStream::Seek</b> method fails, the method will call the <b>IStream::Read</b> method repeatedly until reaching the starting sector.

The DAO-96 standard allows writing of any type of data to CD media. One common usage is to write audio CDs without a 2-second gap between tracks.

DAO-96 also supports variations in the subcode content, such as CD+G and CD-Text.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-writemedia2">IDiscFormat2RawCD::WriteMedia2</a>