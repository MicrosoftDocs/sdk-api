---
UID: NE:bits.BG_ERROR_CONTEXT
title: BG_ERROR_CONTEXT (bits.h)
description: Defines constants that specify the context in which the error occurred.
helpviewer_keywords: ["BG_ERROR_CONTEXT","BG_ERROR_CONTEXT enumeration [BITS]","BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER","BG_ERROR_CONTEXT_GENERAL_TRANSPORT","BG_ERROR_CONTEXT_LOCAL_FILE","BG_ERROR_CONTEXT_NONE","BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION","BG_ERROR_CONTEXT_REMOTE_APPLICATION","BG_ERROR_CONTEXT_REMOTE_FILE","BG_ERROR_CONTEXT_UNKNOWN","_drz_bg_error_context","bits.bg_error_context","bits/BG_ERROR_CONTEXT","bits/BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER","bits/BG_ERROR_CONTEXT_GENERAL_TRANSPORT","bits/BG_ERROR_CONTEXT_LOCAL_FILE","bits/BG_ERROR_CONTEXT_NONE","bits/BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION","bits/BG_ERROR_CONTEXT_REMOTE_APPLICATION","bits/BG_ERROR_CONTEXT_REMOTE_FILE","bits/BG_ERROR_CONTEXT_UNKNOWN"]
old-location: bits\bg_error_context.htm
tech.root: Bits
ms.assetid: c9d98518-6f2e-4fd1-b0ee-6735c6d6ecd9
ms.date: 02/20/2019
ms.keywords: BG_ERROR_CONTEXT, BG_ERROR_CONTEXT enumeration [BITS], BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER, BG_ERROR_CONTEXT_GENERAL_TRANSPORT, BG_ERROR_CONTEXT_LOCAL_FILE, BG_ERROR_CONTEXT_NONE, BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION, BG_ERROR_CONTEXT_REMOTE_APPLICATION, BG_ERROR_CONTEXT_REMOTE_FILE, BG_ERROR_CONTEXT_UNKNOWN, _drz_bg_error_context, bits.bg_error_context, bits/BG_ERROR_CONTEXT, bits/BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER, bits/BG_ERROR_CONTEXT_GENERAL_TRANSPORT, bits/BG_ERROR_CONTEXT_LOCAL_FILE, bits/BG_ERROR_CONTEXT_NONE, bits/BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION, bits/BG_ERROR_CONTEXT_REMOTE_APPLICATION, bits/BG_ERROR_CONTEXT_REMOTE_FILE, bits/BG_ERROR_CONTEXT_UNKNOWN
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: BG_ERROR_CONTEXT
req.redist: 
f1_keywords:
 - BG_ERROR_CONTEXT
 - bits/BG_ERROR_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bits.h
api_name:
 - BG_ERROR_CONTEXT
---

# BG_ERROR_CONTEXT enumeration


## -description

Defines constants that specify the context in which the error occurred.

## -enum-fields

### -field BG_ERROR_CONTEXT_NONE:0

An error has not occurred.

### -field BG_ERROR_CONTEXT_UNKNOWN:1

The error context is unknown.

### -field BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER:2

The transfer queue manager generated the error.

### -field BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION:3

The error was generated while the queue manager was notifying the client of an event.

### -field BG_ERROR_CONTEXT_LOCAL_FILE:4

The error was related to the specified local file. For example, permission was denied, or the volume was unavailable.

### -field BG_ERROR_CONTEXT_REMOTE_FILE:5

The error was related to the specified remote file. For example, the URL was not accessible.

### -field BG_ERROR_CONTEXT_GENERAL_TRANSPORT:6

The transport layer generated the error. These errors are general transport failures (these errors are not specific to the remote file).

### -field BG_ERROR_CONTEXT_REMOTE_APPLICATION:7

The server application to which BITS passed the upload file generated an error while processing the upload file. 

**BITS 1.2 and earlier:** Not supported.

## -see-also

* [IBackgroundCopyError::GetError method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror)
* [IBackgroundCopyError::GetErrorContextDescription method](/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrorcontextdescription)

