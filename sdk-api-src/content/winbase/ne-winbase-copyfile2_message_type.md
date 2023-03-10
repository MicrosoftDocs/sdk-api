---
UID: NE:winbase._COPYFILE2_MESSAGE_TYPE
title: COPYFILE2_MESSAGE_TYPE (winbase.h)
description: Indicates the type of message passed in the COPYFILE2_MESSAGE structure to the CopyFile2ProgressRoutine callback function.
helpviewer_keywords: ["COPYFILE2_CALLBACK_CHUNK_FINISHED","COPYFILE2_CALLBACK_CHUNK_STARTED","COPYFILE2_CALLBACK_ERROR","COPYFILE2_CALLBACK_MAX","COPYFILE2_CALLBACK_NONE","COPYFILE2_CALLBACK_POLL_CONTINUE","COPYFILE2_CALLBACK_STREAM_FINISHED","COPYFILE2_CALLBACK_STREAM_STARTED","COPYFILE2_MESSAGE_TYPE","COPYFILE2_MESSAGE_TYPE enumeration [Files]","fs.copyfile2_message_type","winbase/COPYFILE2_CALLBACK_CHUNK_FINISHED","winbase/COPYFILE2_CALLBACK_CHUNK_STARTED","winbase/COPYFILE2_CALLBACK_ERROR","winbase/COPYFILE2_CALLBACK_MAX","winbase/COPYFILE2_CALLBACK_NONE","winbase/COPYFILE2_CALLBACK_POLL_CONTINUE","winbase/COPYFILE2_CALLBACK_STREAM_FINISHED","winbase/COPYFILE2_CALLBACK_STREAM_STARTED","winbase/COPYFILE2_MESSAGE_TYPE"]
old-location: fs\copyfile2_message_type.htm
tech.root: fs
ms.assetid: 3a16ca3b-79af-4064-82d5-c073d2aa531c
ms.date: 12/05/2018
ms.keywords: COPYFILE2_CALLBACK_CHUNK_FINISHED, COPYFILE2_CALLBACK_CHUNK_STARTED, COPYFILE2_CALLBACK_ERROR, COPYFILE2_CALLBACK_MAX, COPYFILE2_CALLBACK_NONE, COPYFILE2_CALLBACK_POLL_CONTINUE, COPYFILE2_CALLBACK_STREAM_FINISHED, COPYFILE2_CALLBACK_STREAM_STARTED, COPYFILE2_MESSAGE_TYPE, COPYFILE2_MESSAGE_TYPE enumeration [Files], fs.copyfile2_message_type, winbase/COPYFILE2_CALLBACK_CHUNK_FINISHED, winbase/COPYFILE2_CALLBACK_CHUNK_STARTED, winbase/COPYFILE2_CALLBACK_ERROR, winbase/COPYFILE2_CALLBACK_MAX, winbase/COPYFILE2_CALLBACK_NONE, winbase/COPYFILE2_CALLBACK_POLL_CONTINUE, winbase/COPYFILE2_CALLBACK_STREAM_FINISHED, winbase/COPYFILE2_CALLBACK_STREAM_STARTED, winbase/COPYFILE2_MESSAGE_TYPE
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
req.typenames: COPYFILE2_MESSAGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPYFILE2_MESSAGE_TYPE
 - winbase/_COPYFILE2_MESSAGE_TYPE
 - COPYFILE2_MESSAGE_TYPE
 - winbase/COPYFILE2_MESSAGE_TYPE
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
 - COPYFILE2_MESSAGE_TYPE
---

# COPYFILE2_MESSAGE_TYPE enumeration


## -description

Indicates the type of message passed in the 
    <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_message">COPYFILE2_MESSAGE</a> structure to the 
    <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback 
    function.

## -enum-fields

### -field COPYFILE2_CALLBACK_NONE:0

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
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>
