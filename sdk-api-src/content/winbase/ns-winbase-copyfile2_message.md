---
UID: NS:winbase.COPYFILE2_MESSAGE
title: COPYFILE2_MESSAGE (winbase.h)
description: Passed to the CopyFile2ProgressRoutine callback function with information about a pending copy operation.
helpviewer_keywords: ["COPYFILE2_CALLBACK_CHUNK_FINISHED","COPYFILE2_CALLBACK_CHUNK_STARTED","COPYFILE2_CALLBACK_ERROR","COPYFILE2_CALLBACK_POLL_CONTINUE","COPYFILE2_CALLBACK_STREAM_FINISHED","COPYFILE2_CALLBACK_STREAM_STARTED","COPYFILE2_MESSAGE","COPYFILE2_MESSAGE structure [Files]","fs.copyfile2_message","winbase/COPYFILE2_MESSAGE"]
old-location: fs\copyfile2_message.htm
tech.root: fs
ms.assetid: ab841bee-90a0-4beb-99d3-764e608c3872
ms.date: 12/05/2018
ms.keywords: COPYFILE2_CALLBACK_CHUNK_FINISHED, COPYFILE2_CALLBACK_CHUNK_STARTED, COPYFILE2_CALLBACK_ERROR, COPYFILE2_CALLBACK_POLL_CONTINUE, COPYFILE2_CALLBACK_STREAM_FINISHED, COPYFILE2_CALLBACK_STREAM_STARTED, COPYFILE2_MESSAGE, COPYFILE2_MESSAGE structure [Files], fs.copyfile2_message, winbase/COPYFILE2_MESSAGE
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: COPYFILE2_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - COPYFILE2_MESSAGE
 - winbase/COPYFILE2_MESSAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COPYFILE2_MESSAGE
---

# COPYFILE2_MESSAGE structure


## -description

Passed to the 
    <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback function with 
    information about a pending copy operation.

## -struct-fields

### -field Type

Value from the <a href="/windows/desktop/api/winbase/ne-winbase-copyfile2_message_type">COPYFILE2_MESSAGE_TYPE</a> 
      enumeration used as a discriminant for the <b>Info</b> union within this structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_CHUNK_STARTED"></a><a id="copyfile2_callback_chunk_started"></a><dl>
<dt><b>COPYFILE2_CALLBACK_CHUNK_STARTED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Indicates a single chunk of a stream has started to be copied. Information is in the 
        <b>ChunkStarted</b> structure within the <b>Info</b> 
        union.

</td>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_CHUNK_FINISHED"></a><a id="copyfile2_callback_chunk_finished"></a><dl>
<dt><b>COPYFILE2_CALLBACK_CHUNK_FINISHED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Indicates the copy of a single chunk of a stream has completed. Information is in the 
        <b>ChunkFinished</b> structure within the <b>Info</b> 
        union.

</td>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_STREAM_STARTED"></a><a id="copyfile2_callback_stream_started"></a><dl>
<dt><b>COPYFILE2_CALLBACK_STREAM_STARTED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Indicates both source and destination handles for a stream have been opened and the  copy of the stream 
        is about to be started. Information is in the <b>StreamStarted</b> structure within 
        the <b>Info</b> union. This does not indicate that the copy has started for that stream.

</td>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_STREAM_FINISHED"></a><a id="copyfile2_callback_stream_finished"></a><dl>
<dt><b>COPYFILE2_CALLBACK_STREAM_FINISHED</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Indicates the copy operation for a stream have started to be completed, either successfully or due to a 
        <b>COPYFILE2_PROGRESS_STOP</b> return from 
        <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a>.  Information is 
        in the <b>StreamFinished</b> structure within the <b>Info</b> 
        union.

</td>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_POLL_CONTINUE"></a><a id="copyfile2_callback_poll_continue"></a><dl>
<dt><b>COPYFILE2_CALLBACK_POLL_CONTINUE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
May be sent periodically.  Information is in the 
        <b>PollContinue</b> structure within the <b>Info</b> 
        union.

</td>
</tr>
<tr>
<td width="40%"><a id="COPYFILE2_CALLBACK_ERROR"></a><a id="copyfile2_callback_error"></a><dl>
<dt><b>COPYFILE2_CALLBACK_ERROR</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
An error was encountered during the copy operation.  Information is in the 
        <b>Error</b> structure within the <b>Info</b> 
        union.

</td>
</tr>
</table>

### -field dwPadding

### -field Info

### -field Info.ChunkStarted

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_CHUNK_STARTED</b> (1).

### -field Info.ChunkStarted.dwStreamNumber

Indicates which stream within the file is about to be copied. The value used for identifying a stream 
        within a file will start at one (1) and will always be higher than any previous stream for that file.

### -field Info.ChunkStarted.dwReserved

This member is reserved for internal use.

### -field Info.ChunkStarted.hSourceFile

Handle to the source stream.

### -field Info.ChunkStarted.hDestinationFile

Handle to the destination stream.

### -field Info.ChunkStarted.uliChunkNumber

Indicates which chunk within the current stream is about to be copied. The value used for a chunk will 
        start at zero (0) and will always be higher than that of any previous chunk for the current stream.

### -field Info.ChunkStarted.uliChunkSize

Size of the copied chunk, in bytes.

### -field Info.ChunkStarted.uliStreamSize

Size of the current stream, in bytes.

### -field Info.ChunkStarted.uliTotalFileSize

Size of all streams for this file, in bytes.

### -field Info.ChunkFinished

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_CHUNK_FINISHED</b> (2).



##### ChunkFinished.dwReserved

This member is reserved for internal use.

### -field Info.ChunkFinished.dwStreamNumber

Indicates which stream within the file is about to be copied. The value used for identifying a stream 
        within a file will start at one (1) and will always be higher than any previous stream for that file.

### -field Info.ChunkFinished.dwFlags

### -field Info.ChunkFinished.hSourceFile

Handle to the source stream.

### -field Info.ChunkFinished.hDestinationFile

Handle to the destination stream.

### -field Info.ChunkFinished.uliChunkNumber

Indicates which chunk within the current stream is in process. The value used for a chunk will start at 
        zero (0) and will always be higher than that of any previous chunk for the current stream.

### -field Info.ChunkFinished.uliChunkSize

Size of the copied chunk, in bytes.

### -field Info.ChunkFinished.uliStreamSize

Size of the current stream, in bytes.

### -field Info.ChunkFinished.uliStreamBytesTransferred

Total bytes copied for this stream so far.

### -field Info.ChunkFinished.uliTotalFileSize

Size of all streams for this file, in bytes.

### -field Info.ChunkFinished.uliTotalBytesTransferred

Total bytes copied for this file so far.

### -field Info.StreamStarted

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_STREAM_STARTED</b> (3).

### -field Info.StreamStarted.dwStreamNumber

Indicates which stream within the file is about to be copied. The value used for identifying a stream 
        within a file will start at one (1) and will always be higher than any previous stream for that file.

### -field Info.StreamStarted.dwReserved

This member is reserved for internal use.

### -field Info.StreamStarted.hSourceFile

Handle to the source stream.

### -field Info.StreamStarted.hDestinationFile

Handle to the destination stream.

### -field Info.StreamStarted.uliStreamSize

Size of the current stream, in bytes.

### -field Info.StreamStarted.uliTotalFileSize

Size of all streams for this file, in bytes.

### -field Info.StreamFinished

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_STREAM_FINISHED</b> (4).

### -field Info.StreamFinished.dwStreamNumber

Indicates which stream within the file is about to be copied. The value used for identifying a stream 
        within a file will start at one (1) and will always be higher than any previous stream for that file.

### -field Info.StreamFinished.dwReserved

This member is reserved for internal use.

### -field Info.StreamFinished.hSourceFile

Handle to the source stream.

### -field Info.StreamFinished.hDestinationFile

Handle to the destination stream.

### -field Info.StreamFinished.uliStreamSize

Size of the current stream, in bytes.

### -field Info.StreamFinished.uliStreamBytesTransferred

Total bytes copied for this stream so far.

### -field Info.StreamFinished.uliTotalFileSize

Size of all streams for this file, in bytes.

### -field Info.StreamFinished.uliTotalBytesTransferred

Total bytes copied for this file so far.

### -field Info.PollContinue

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_POLL_CONTNUE</b> (5).

### -field Info.PollContinue.dwReserved

This member is reserved for internal use.

### -field Info.Error

This structure is selected if the <b>Type</b> member is set to 
       <b>COPYFILE2_CALLBACK_ERROR</b> (6).

### -field Info.Error.CopyPhase

Value from the <a href="/windows/desktop/api/winbase/ne-winbase-copyfile2_copy_phase">COPYFILE2_COPY_PHASE</a> 
        enumeration indicating the current phase of the copy at the time of the error.

### -field Info.Error.dwStreamNumber

The number of the stream that was being processed at the time of the error.

### -field Info.Error.hrFailure

Value indicating the problem.

### -field Info.Error.dwReserved

This member is reserved for internal use.

### -field Info.Error.uliChunkNumber

Indicates which chunk within the current stream was being processed at the time of the error. The value 
        used for a chunk will start at zero (0) and will always be higher than that of any previous chunk for the 
        current stream.

### -field Info.Error.uliStreamSize

Size, in bytes, of the stream being processed.

### -field Info.Error.uliStreamBytesTransferred

Number of bytes that had been successfully transferred for the stream being processed.

### -field Info.Error.uliTotalFileSize

Size, in bytes, of the total file being processed.

### -field Info.Error.uliTotalBytesTransferred

Number of bytes that had been successfully transferred for the entire copy operation.

## -remarks

To compile an application that uses the 
    <b>COPYFILE2_MESSAGE</b> structure, define the 
    <b>_WIN32_WINNT</b> macro as 0x0601 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.