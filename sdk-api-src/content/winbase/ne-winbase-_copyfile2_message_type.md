---
UID: NE:winbase._COPYFILE2_MESSAGE_TYPE
title: "_COPYFILE2_MESSAGE_TYPE"
author: windows-sdk-content
description: Indicates the type of message passed in the COPYFILE2_MESSAGE structure to the CopyFile2ProgressRoutine callback function.
old-location: fs\copyfile2_message_type.htm
old-project: fileio
ms.assetid: 3a16ca3b-79af-4064-82d5-c073d2aa531c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: COPYFILE2_CALLBACK_CHUNK_FINISHED, COPYFILE2_CALLBACK_CHUNK_STARTED, COPYFILE2_CALLBACK_ERROR, COPYFILE2_CALLBACK_MAX, COPYFILE2_CALLBACK_NONE, COPYFILE2_CALLBACK_POLL_CONTINUE, COPYFILE2_CALLBACK_STREAM_FINISHED, COPYFILE2_CALLBACK_STREAM_STARTED, COPYFILE2_MESSAGE_TYPE, COPYFILE2_MESSAGE_TYPE enumeration [Files], _COPYFILE2_MESSAGE_TYPE, fs.copyfile2_message_type, winbase/COPYFILE2_CALLBACK_CHUNK_FINISHED, winbase/COPYFILE2_CALLBACK_CHUNK_STARTED, winbase/COPYFILE2_CALLBACK_ERROR, winbase/COPYFILE2_CALLBACK_MAX, winbase/COPYFILE2_CALLBACK_NONE, winbase/COPYFILE2_CALLBACK_POLL_CONTINUE, winbase/COPYFILE2_CALLBACK_STREAM_FINISHED, winbase/COPYFILE2_CALLBACK_STREAM_STARTED, winbase/COPYFILE2_MESSAGE_TYPE
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
req.typenames: COPYFILE2_MESSAGE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COPYFILE2_MESSAGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _COPYFILE2_MESSAGE_TYPE enumeration


## -description


Indicates the type of message passed in the 
    <a href="https://msdn.microsoft.com/ab841bee-90a0-4beb-99d3-764e608c3872">COPYFILE2_MESSAGE</a> structure to the 
    <a href="https://msdn.microsoft.com/d14b5f5b-c353-49e8-82bb-a695a3ec76fd">CopyFile2ProgressRoutine</a> callback 
    function.


## -enum-fields




### -field COPYFILE2_CALLBACK_NONE

Not a valid value.


### -field COPYFILE2_CALLBACK_CHUNK_STARTED

Indicates a single chunk of a stream has started to be copied.


### -field COPYFILE2_CALLBACK_CHUNK_FINISHED

Indicates the copy of a single chunk of a stream has completed.


### -field COPYFILE2_CALLBACK_STREAM_STARTED

Indicates both source and destination handles for a stream have been opened and the  copy of the stream is 
      about to be started.


### -field COPYFILE2_CALLBACK_STREAM_FINISHED

Indicates the copy operation for a stream have started to be completed.


### -field COPYFILE2_CALLBACK_POLL_CONTINUE

May be sent periodically.


### -field COPYFILE2_CALLBACK_ERROR


### -field COPYFILE2_CALLBACK_MAX

An error was encountered during the copy operation.


## -remarks



To compile an application that uses this enumeration, define the <b>_WIN32_WINNT</b> 
    macro as 0x0601 or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>
 

 

