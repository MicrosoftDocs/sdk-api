---
UID: NF:imapi2.IDiscFormat2Data.Write
title: IDiscFormat2Data::Write (imapi2.h)
description: Writes the data stream to the device.
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","Write method","IDiscFormat2Data.Write","IDiscFormat2Data::Write","Write","Write method [IMAPI]","Write method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_write","imapi2/IDiscFormat2Data::Write"]
old-location: imapi\idiscformat2data_write.htm
tech.root: imapi
ms.assetid: 9daf31f3-84c2-48b2-ab21-a3809b6ed9af
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],Write method, IDiscFormat2Data.Write, IDiscFormat2Data::Write, Write, Write method [IMAPI], Write method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_write, imapi2/IDiscFormat2Data::Write
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
 - IDiscFormat2Data::Write
 - imapi2/IDiscFormat2Data::Write
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
 - IDiscFormat2Data.Write
---

# IDiscFormat2Data::Write


## -description

Writes the data stream to the device.<div class="alert"><b>Note</b>   For write success, the size of the passed-in stream must be a multiple of the sector size, 2048. This includes operations that utilize streams associated with .iso images not created by IMAPI.</div>
<div> </div>

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
<dt><b>E_IMAPI_UNEXPECTED_RESPONSE_FROM_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The write failed because the drive returned error information that could not be recovered from.

Value: 0xC0AA0301

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2DATA_RECORDER_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This device does not support the operations required by this disc format.

Value: 0xC0AA0407

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
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2DATA_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0400

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2DATA_STREAM_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The size of the provided <b>IStream</b> object is invalid. The size must be a multiple of the sector size, 2048.

Value: 0xC0AA0403

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2DATA_MEDIA_IS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The current media type is unsupported.

Value: (HRESULT)0xC0AA0406

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -remarks

Before calling this method, you must call the following methods:

<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-iwriteengine2-put_recorder">IDiscFormat2Data::put_Recorder</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_clientname">IDiscFormat2Data::put_ClientName</a>
</li>
</ul>
You should also consider calling the following methods if their default values are not appropriate for your application:

<ul>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_bufferunderrunfreedisabled">IDiscFormat2Data::put_BufferUnderrunFreeDisabled</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_disableconsumerdvdcompatibilitymode">IDiscFormat2Data::put_DisableConsumerDvdCompatibilityMode</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_forcemediatobeclosed">IDiscFormat2Data::put_ForceMediaToBeClosed</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_forceoverwrite">IDiscFormat2Data::put_ForceOverwrite</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_postgapalreadyinimage">IDiscFormat2Data::put_PostgapAlreadyInImage</a>
</li>
<li>
<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-setwritespeed">IDiscFormat2Data::SetWriteSpeed</a>
</li>
</ul>
This method is synchronous, which means that control is not returned until the provided <b>IStream</b> is recorded to the media. To determine the progress of the write operation, you must implement the <a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a> interface. For examples that show how to implement an event handler in a script, see <a href="/windows/desktop/imapi/monitoring-progress-with-events">Monitoring Progress With Events</a>.

On sequentially recorded discs, the provided <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> is recorded as a new session. On rewritable discs, the provided <b>IStream</b> is always recorded starting from sector 0, but the object providing the <b>IStream</b> interface can also provide the <a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist">IBlockRangeList</a> interface listing the sectors that need to be recorded. The <b>IBlockRangeList</b> interface is used to avoid rewriting of sectors that have not changed in multisession scenarios. If the object providing <b>IStream</b> does not provide <b>IBlockRangeList</b>, it is assumed that the entire <b>IStream</b> needs to be recorded.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-cancelwrite">IDiscFormat2Data::CancelWrite</a>