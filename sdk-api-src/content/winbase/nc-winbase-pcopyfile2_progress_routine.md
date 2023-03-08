---
UID: NC:winbase.PCOPYFILE2_PROGRESS_ROUTINE
title: PCOPYFILE2_PROGRESS_ROUTINE (winbase.h)
description: An application-defined callback function used with the CopyFile2 function.
helpviewer_keywords: ["CopyFile2ProgressRoutine","CopyFile2ProgressRoutine callback function [Files]","PCOPYFILE2_PROGRESS_ROUTINE","PCOPYFILE2_PROGRESS_ROUTINE callback","fs.copyfile2progressroutine","winbase/CopyFile2ProgressRoutine","winbase/PCOPYFILE2_PROGRESS_ROUTINE"]
old-location: fs\copyfile2progressroutine.htm
tech.root: fs
ms.assetid: d14b5f5b-c353-49e8-82bb-a695a3ec76fd
ms.date: 12/05/2018
ms.keywords: CopyFile2ProgressRoutine, CopyFile2ProgressRoutine callback function [Files], PCOPYFILE2_PROGRESS_ROUTINE, PCOPYFILE2_PROGRESS_ROUTINE callback, fs.copyfile2progressroutine, winbase/CopyFile2ProgressRoutine, winbase/PCOPYFILE2_PROGRESS_ROUTINE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PCOPYFILE2_PROGRESS_ROUTINE
 - winbase/PCOPYFILE2_PROGRESS_ROUTINE
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
 - CopyFile2ProgressRoutine
 - PCOPYFILE2_PROGRESS_ROUTINE
---

# PCOPYFILE2_PROGRESS_ROUTINE callback function


## -description

An application-defined callback function used with the 
    <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> function. It is called when a portion of 
    a copy or move operation is completed. The <b>PCOPYFILE2_PROGRESS_ROUTINE</b> type defines a 
    pointer to this callback function. 
    <b>CopyFile2ProgressRoutine</b> is a placeholder for the 
    application-defined function name.

## -parameters

### -param pMessage [in]

Pointer to a <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_message">COPYFILE2_MESSAGE</a> structure.

### -param pvCallbackContext [in, optional]

Copy of value passed in the <b>pvCallbackContext</b> member of the 
      <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> structure 
      passed to <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a>.

## -returns

Value from the <a href="/windows/desktop/api/winbase/ne-winbase-copyfile2_message_action">COPYFILE2_MESSAGE_ACTION</a> 
      enumeration indicating what action should be taken.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYFILE2_PROGRESS_CONTINUE</b></dt>
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
<dt><b>COPYFILE2_PROGRESS_CANCEL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Cancel the copy operation. The <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> function 
        will fail, return 
        <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> and any 
        partially copied fragments will be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYFILE2_PROGRESS_STOP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Stop the copy operation. The <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> function will 
        fail, return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> 
        and any partially copied fragments will be left intact. The operation can be restarted using the 
        <b>COPY_FILE_RESUME_FROM_PAUSE</b> flag only if 
        <b>COPY_FILE_RESTARTABLE</b> was set in the <b>dwCopyFlags</b> member 
        of the <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> 
        structure passed to the <b>CopyFile2</b> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYFILE2_PROGRESS_QUIET</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Continue the copy operation but do not call the 
        <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback function 
        again for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COPYFILE2_PROGRESS_PAUSE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Pause the copy operation. In most cases the <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> 
        function will fail and return 
        <code>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</code> and any 
        partially copied fragments will be left intact (except for the header written that is used to resume the copy 
        operation later.) In case the copy operation was complete at the time the pause request is processed the 
        <b>CopyFile2</b> call will complete successfully and no resume 
        header will be written.

</td>
</tr>
</table>

## -remarks

The <b>COPYFILE2_CALLBACK_STREAM_FINISHED</b> message is the last message for a paused 
    copy. If <b>COPYFILE2_PROGRESS_PAUSE</b> is returned in response to a 
    <b>COPYFILE2_CALLBACK_STREAM_FINISHED</b> message then no further callbacks will be sent.

To compile an application that uses the <b>PCOPYFILE2_PROGRESS_ROUTINE</b> 
    function pointer type, define the <b>_WIN32_WINNT</b> macro as 0x0601 or later. For more 
    information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
