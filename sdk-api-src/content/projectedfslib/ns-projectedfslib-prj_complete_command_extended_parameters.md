---
UID: NS:projectedfslib.PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
title: PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS (projectedfslib.h)
description: Specifies parameters required for completing certain callbacks.
helpviewer_keywords: ["PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS","PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS structure","ProjFS.prj_complete_command_extended_parameters","projectedfslib/PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS"]
old-location: projfs\prj_complete_command_extended_parameters.htm
tech.root: ProjFS
ms.assetid: 1E13CED8-41DF-4206-AA60-751424424011
ms.date: 12/05/2018
ms.keywords: PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS, PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS structure, ProjFS.prj_complete_command_extended_parameters, projectedfslib/PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
 - projectedfslib/PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS
---

# PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS structure


## -description

Specifies parameters required for completing certain callbacks.

## -struct-fields

### -field CommandType

The type of command.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Notification

### -field DUMMYUNIONNAME.Notification.NotificationMask

A new set of notifications the provider wishes to receive.

### -field DUMMYUNIONNAME.Enumeration

### -field DUMMYUNIONNAME.Enumeration.DirEntryBufferHandle

An opaque handle to a directory entry buffer. This must be the value passed in the dirEntryBufferHandle parameter of the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback being completed.



## -remarks

For any callback except <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb">PRJ_CANCEL_COMMAND_CB</a>, the provider may opt to process the callback asynchronously. To do so it returns HRESULT_FROM_WIN32(ERROR_IO_PENDING) from the callback. Once the provider has finished processing the callback. 

If the provider calls this function for the commandId passed by the <a href="/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb">PRJ_CANCEL_COMMAND_CB</a> callback it is not an error, however it is a no-op because the I/O that caused the callback invocation identified by commandId has already ended.