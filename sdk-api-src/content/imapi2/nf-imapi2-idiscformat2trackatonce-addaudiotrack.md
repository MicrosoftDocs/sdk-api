---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.AddAudioTrack
title: IDiscFormat2TrackAtOnce::AddAudioTrack
author: windows-sdk-content
description: Writes the data stream to the current media as a new track.
old-location: imapi\idiscformat2trackatonce_addaudiotrack.htm
tech.root: imapi
ms.assetid: 3ac74b91-b0c7-471f-b6a9-1393d677e0c1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddAudioTrack, AddAudioTrack method [IMAPI], AddAudioTrack method [IMAPI],IDiscFormat2TrackAtOnce interface, IDiscFormat2TrackAtOnce interface [IMAPI],AddAudioTrack method, IDiscFormat2TrackAtOnce.AddAudioTrack, IDiscFormat2TrackAtOnce::AddAudioTrack, imapi.idiscformat2trackatonce_addaudiotrack, imapi2/IDiscFormat2TrackAtOnce::AddAudioTrack
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDiscFormat2TrackAtOnce.AddAudioTrack
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2TrackAtOnce::AddAudioTrack


## -description


Writes the data stream to the current media as a new track.


## -parameters




### -param data [in]

An <b>IStream</b> interface of the audio data to write as the next track on the media.

The data format contains 44.1KHz, 16-bit stereo, raw audio samples. This is the same format used by the audio samples in a Microsoft WAV audio file (without the header).


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
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0502

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0500

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_TRACK_LIMIT_REACHED</b></dt>
</dl>
</td>
<td width="60%">
CD-R and CD-RW media support a maximum of 99 audio tracks.

Value: 0xC0AA0508

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_STREAM_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provided audio stream is not valid.

Value: 0xC0AA050D

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_NOT_ENOUGH_SPACE</b></dt>
</dl>
</td>
<td width="60%">
There is not enough space left on the media to add the provided audio track.

Value: 0xC0AA0509

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



Before calling this method, you must call the <a href="https://msdn.microsoft.com/6d67b076-0c3f-4d1f-aa19-8e22dd98f331">IDiscFormat2TrackAtOnce::put_Recorder</a> and <a href="https://msdn.microsoft.com/29a0a857-c515-4265-b0b6-6e2048f3de18">IDiscFormat2TrackAtOnce::PrepareMedia</a> methods.

You should also consider calling the following methods if their default values are not appropriate for your application:

<ul>
<li>
<a href="https://msdn.microsoft.com/93a19bd7-9302-49f5-a5e5-573bf72725a3">IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9140aa9f-f592-4ef4-85c7-321e5503b0b8">IDiscFormat2TrackAtOnce::put_ClientName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ffde10f9-259a-400d-b83e-f8c81bbe8f94">IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia</a>
</li>
</ul>
To determine the progress of the write operation, you must implement the <a href="https://msdn.microsoft.com/15d88768-f6e9-4d0a-a132-08f89fb3c34f">DDiscFormat2TrackAtOnceEvents</a> interface. For examples that show how to implement an event handler in a script, see <a href="https://msdn.microsoft.com/1f15a5fe-f5d7-4e09-805f-2d0380bf2bb2">Monitoring Progress With Events</a>.

The media can accommodate 99 tracks of audio data. Track numbering starts at 1. The last track is 99.

Silence, or data samples containing zeroes, will be added to the track-writing operation in the following ways:

<ul>
<li>The minimum track size is 4 seconds and if needed, the track data will be enlarged to meet this requirement. </li>
<li>Due to the nature of track-at-once recording, a two-second gap is added between successive audio tracks.  This gap is normally hidden by PC-based players, but may be noticeable on some consumer electronics equipment.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/27f2d248-1c83-4784-82f9-75ce0a038b87">IDiscFormat2TrackAtOnce</a>



<a href="https://msdn.microsoft.com/09e71d36-da1d-4ba0-bd6b-4ce4425d481a">IDiscFormat2TrackAtOnce::CancelAddTrack</a>
 

 

