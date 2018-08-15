---
UID: NE:winbase._COPYFILE2_MESSAGE_ACTION
title: "_COPYFILE2_MESSAGE_ACTION"
author: windows-sdk-content
description: Returned by the CopyFile2ProgressRoutine callback function to indicate what action should be taken for the pending copy operation.
old-location: fs\copyfile2_message_action.htm
old-project: fileio
ms.assetid: 0beae28e-f493-4ae1-a4d9-3df69de166b7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: COPYFILE2_MESSAGE_ACTION, COPYFILE2_MESSAGE_ACTION enumeration [Files], COPYFILE2_PROGRESS_CANCEL, COPYFILE2_PROGRESS_CONTINUE, COPYFILE2_PROGRESS_PAUSE, COPYFILE2_PROGRESS_QUIET, COPYFILE2_PROGRESS_STOP, _COPYFILE2_MESSAGE_ACTION, fs.copyfile2_message_action, winbase/COPYFILE2_MESSAGE_ACTION, winbase/COPYFILE2_PROGRESS_CANCEL, winbase/COPYFILE2_PROGRESS_CONTINUE, winbase/COPYFILE2_PROGRESS_PAUSE, winbase/COPYFILE2_PROGRESS_QUIET, winbase/COPYFILE2_PROGRESS_STOP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: COPYFILE2_MESSAGE_ACTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COPYFILE2_MESSAGE_ACTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _COPYFILE2_MESSAGE_ACTION enumeration


## -description


Returned by the 
    <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> callback function to 
    indicate what action should be taken for the pending copy operation.


## -enum-fields




### -field COPYFILE2_PROGRESS_CONTINUE

Continue the copy operation.


### -field COPYFILE2_PROGRESS_CANCEL

Cancel the copy operation. The <a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a> call will fail 
      and return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> and 
      any partially copied fragments will be deleted.


### -field COPYFILE2_PROGRESS_STOP

Stop the copy operation. The <a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a> call will fail 
      and return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_ABORTED)</code> and 
      any partially copied fragments will be left intact. The operation can be restarted using the 
      <b>COPY_FILE_RESUME_FROM_PAUSE</b> flag only if the 
      <b>COPY_FILE_RESTARTABLE</b> flag was set in the <b>dwCopyFlags</b> 
      member of the 
      <a href="https://msdn.microsoft.com/a8da62e5-bc49-4aff-afaa-e774393b7120">COPYFILE2_EXTENDED_PARAMETERS</a> structure 
      passed to the <b>CopyFile2</b> function.


### -field COPYFILE2_PROGRESS_QUIET

Continue the copy operation but do not call the 
      <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> callback function 
      again for this operation.


### -field COPYFILE2_PROGRESS_PAUSE

Pause the copy operation and write a restart header. This value is not compatible with the 
      <b>COPY_FILE_RESTARTABLE</b> flag  for the <b>dwCopyFlags</b> member of 
      the <a href="https://msdn.microsoft.com/a8da62e5-bc49-4aff-afaa-e774393b7120">COPYFILE2_EXTENDED_PARAMETERS</a> 
      structure. In most cases the <a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a> call will fail and 
      return <code>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</code> and any 
      partially copied fragments will be left intact (except for the header written that is used to resume the copy 
      operation later.) In case the copy operation was complete at the time the pause request is processed the 
      <b>CopyFile2</b> call will complete successfully and no resume 
      header will be written. After this value is processed one more callback will be made to the 
      <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> with the message 
      specifying a <b>COPYFILE2_CALLBACK_STREAM_FINISHED</b> (4) value in the 
      <b>Type</b> member of the 
      <a href="https://msdn.microsoft.com/ab841bee-90a0-4beb-99d3-764e608c3872">COPYFILE2_MESSAGE</a> structure. After the callback has 
      returned CopyFile2 will fail with 
      <code>HRESULT_FROM_WIN32(ERROR_REQUEST_PAUSED)</code>.


## -remarks



To compile an application that uses this enumeration, define the <b>_WIN32_WINNT</b> 
    macro as 0x0601 or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/aa2df686-4b61-4d90-ba0b-c78c5a0d2d59">CopyFile2</a>



<a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a>



<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>
 

 

