---
UID: NC:winbase.LPPROGRESS_ROUTINE
title: LPPROGRESS_ROUTINE (winbase.h)
description: An application-defined callback function used with the CopyFileEx, MoveFileTransacted, and MoveFileWithProgress functions.
helpviewer_keywords: ["CALLBACK_CHUNK_FINISHED","CALLBACK_STREAM_SWITCH","CopyProgressRoutine","CopyProgressRoutine callback","CopyProgressRoutine callback function [Files]","LPPROGRESS_ROUTINE","LPPROGRESS_ROUTINE callback function [Files]","_win32_copyprogressroutine","base.copyprogressroutine","fs.copyprogressroutine","winbase/CopyProgressRoutine","winbase/LPPROGRESS_ROUTINE"]
old-location: fs\copyprogressroutine.htm
tech.root: fs
ms.assetid: 2c02b212-d4ac-4b01-8955-2561d8c42b1b
ms.date: 12/05/2018
ms.keywords: CALLBACK_CHUNK_FINISHED, CALLBACK_STREAM_SWITCH, CopyProgressRoutine, CopyProgressRoutine callback, CopyProgressRoutine callback function [Files], LPPROGRESS_ROUTINE, LPPROGRESS_ROUTINE callback function [Files], _win32_copyprogressroutine, base.copyprogressroutine, fs.copyprogressroutine, winbase/CopyProgressRoutine, winbase/LPPROGRESS_ROUTINE
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPPROGRESS_ROUTINE
 - winbase/LPPROGRESS_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinBase.h
api_name:
 - CopyProgressRoutine
 - LPPROGRESS_ROUTINE
---

# LPPROGRESS_ROUTINE callback function


## -description

An application-defined callback function used with the 
    <a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>, 
    <a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>, and 
    <a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a> functions. It is 
    called when a portion of a copy or move operation is completed. The 
    <b>LPPROGRESS_ROUTINE</b> type defines a pointer to this callback function. 
    <b>CopyProgressRoutine</b> is a placeholder for the 
    application-defined function name.

## -parameters

### -param TotalFileSize [in]

The total size of the file, in bytes.

### -param TotalBytesTransferred [in]

The total number of bytes transferred from the source file to the destination file since the copy operation 
      began.

### -param StreamSize [in]

The total size of the current file stream, in bytes.

### -param StreamBytesTransferred [in]

The total number of bytes in the current stream that have been transferred from the source file to the 
      destination file since the copy operation began.

### -param dwStreamNumber [in]

A handle to the current stream. The first time 
      <b>CopyProgressRoutine</b> is called, the stream number 
      is 1.

### -param dwCallbackReason [in]

The reason that <b>CopyProgressRoutine</b> was 
      called. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALLBACK_CHUNK_FINISHED"></a><a id="callback_chunk_finished"></a><dl>
<dt><b>CALLBACK_CHUNK_FINISHED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Another part of the data file was copied.

</td>
</tr>
<tr>
<td width="40%"><a id="CALLBACK_STREAM_SWITCH"></a><a id="callback_stream_switch"></a><dl>
<dt><b>CALLBACK_STREAM_SWITCH</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Another stream was created and is about to be copied. This is the callback reason given when the callback 
        routine is first invoked.

</td>
</tr>
</table>

### -param hSourceFile [in]

A handle to the source file.

### -param hDestinationFile [in]

A handle to the destination file

### -param lpData [in, optional]

Argument passed to <b>CopyProgressRoutine</b> by 
      <a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>, 
      <a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>, or 
      <a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>.

## -returns

The <b>CopyProgressRoutine</b> function should return 
       one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PROGRESS_CANCEL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Cancel the copy operation and delete the destination file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PROGRESS_CONTINUE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Continue the copy operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PROGRESS_QUIET</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Continue the copy operation, but stop invoking 
        <a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> to report progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PROGRESS_STOP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Stop the copy operation. It can be restarted at a later time.

</td>
</tr>
</table>

## -remarks

An application can use this information to display a progress bar that shows the total number of bytes copied 
    as a percent of the total file size.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfileexa">CopyFileEx</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefiletransacteda">MoveFileTransacted</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>