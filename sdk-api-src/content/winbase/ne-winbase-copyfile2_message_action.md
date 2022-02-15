---
UID: NE:winbase._COPYFILE2_MESSAGE_ACTION
title: COPYFILE2_MESSAGE_ACTION (winbase.h)
description: Returned by the CopyFile2ProgressRoutine callback function to indicate what action should be taken for the pending copy operation.
helpviewer_keywords: ["COPYFILE2_MESSAGE_ACTION","COPYFILE2_MESSAGE_ACTION enumeration [Files]","COPYFILE2_PROGRESS_CANCEL","COPYFILE2_PROGRESS_CONTINUE","COPYFILE2_PROGRESS_PAUSE","COPYFILE2_PROGRESS_QUIET","COPYFILE2_PROGRESS_STOP","fs.copyfile2_message_action","winbase/COPYFILE2_MESSAGE_ACTION","winbase/COPYFILE2_PROGRESS_CANCEL","winbase/COPYFILE2_PROGRESS_CONTINUE","winbase/COPYFILE2_PROGRESS_PAUSE","winbase/COPYFILE2_PROGRESS_QUIET","winbase/COPYFILE2_PROGRESS_STOP"]
old-location: fs\copyfile2_message_action.htm
tech.root: fs
ms.assetid: 0beae28e-f493-4ae1-a4d9-3df69de166b7
ms.date: 12/05/2018
ms.keywords: COPYFILE2_MESSAGE_ACTION, COPYFILE2_MESSAGE_ACTION enumeration [Files], COPYFILE2_PROGRESS_CANCEL, COPYFILE2_PROGRESS_CONTINUE, COPYFILE2_PROGRESS_PAUSE, COPYFILE2_PROGRESS_QUIET, COPYFILE2_PROGRESS_STOP, fs.copyfile2_message_action, winbase/COPYFILE2_MESSAGE_ACTION, winbase/COPYFILE2_PROGRESS_CANCEL, winbase/COPYFILE2_PROGRESS_CONTINUE, winbase/COPYFILE2_PROGRESS_PAUSE, winbase/COPYFILE2_PROGRESS_QUIET, winbase/COPYFILE2_PROGRESS_STOP
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
req.typenames: COPYFILE2_MESSAGE_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPYFILE2_MESSAGE_ACTION
 - winbase/_COPYFILE2_MESSAGE_ACTION
 - COPYFILE2_MESSAGE_ACTION
 - winbase/COPYFILE2_MESSAGE_ACTION
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
 - COPYFILE2_MESSAGE_ACTION
---

# COPYFILE2_MESSAGE_ACTION enumeration


## -description

Returned by the 
    <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback function to 
    indicate what action should be taken for the pending copy operation.

## -enum-fields

### -field COPYFILE2_PROGRESS_CONTINUE:0

Continue the copy operation.

### -field COPYFILE2_PROGRESS_CANCEL

Cancel the copy operation. The <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> call will fail 
      and return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> and 
      any partially copied fragments will be deleted.

### -field COPYFILE2_PROGRESS_STOP

Stop the copy operation. The <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> call will fail 
      and return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> and 
      any partially copied fragments will be left intact. The operation can be restarted using the 
      <b>COPY_FILE_RESUME_FROM_PAUSE</b> flag only if the 
      <b>COPY_FILE_RESTARTABLE</b> flag was set in the <b>dwCopyFlags</b> 
      member of the 
      <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> structure 
      passed to the <b>CopyFile2</b> function.

### -field COPYFILE2_PROGRESS_QUIET

Continue the copy operation but do not call the 
      <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback function 
      again for this operation.

### -field COPYFILE2_PROGRESS_PAUSE

Pause the copy operation and write a restart header. This value is not compatible with the 
      <b>COPY_FILE_RESTARTABLE</b> flag  for the <b>dwCopyFlags</b> member of 
      the <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_extended_parameters">COPYFILE2_EXTENDED_PARAMETERS</a> 
      structure. In most cases the <a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a> call will fail and 
      return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</code> and any 
      partially copied fragments will be left intact (except for the header written that is used to resume the copy 
      operation later.) In case the copy operation was complete at the time the pause request is processed the 
      <b>CopyFile2</b> call will complete successfully and no resume 
      header will be written. After this value is processed one more callback will be made to the 
      <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> with the message 
      specifying a <b>COPYFILE2_CALLBACK_STREAM_FINISHED</b> (4) value in the 
      <b>Type</b> member of the 
      <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_message">COPYFILE2_MESSAGE</a> structure. After the callback has 
      returned CopyFile2 will fail with 
      <code>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</code>.

## -remarks

To compile an application that uses this enumeration, define the <b>_WIN32_WINNT</b> 
    macro as 0x0601 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a>



<a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a>



<a href="/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>
