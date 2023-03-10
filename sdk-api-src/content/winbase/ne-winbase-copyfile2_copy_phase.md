---
UID: NE:winbase._COPYFILE2_COPY_PHASE
title: COPYFILE2_COPY_PHASE (winbase.h)
description: Indicates the phase of a copy at the time of an error.
helpviewer_keywords: ["COPYFILE2_COPY_PHASE","COPYFILE2_COPY_PHASE enumeration [Files]","COPYFILE2_PHASE_MAX","COPYFILE2_PHASE_NAMEGRAFT_COPY","COPYFILE2_PHASE_NONE","COPYFILE2_PHASE_PREPARE_DEST","COPYFILE2_PHASE_PREPARE_SOURCE","COPYFILE2_PHASE_READ_SOURCE","COPYFILE2_PHASE_SERVER_COPY","COPYFILE2_PHASE_WRITE_DESTINATION","fs.copyfile2_copy_phase","winbase/COPYFILE2_COPY_PHASE","winbase/COPYFILE2_PHASE_MAX","winbase/COPYFILE2_PHASE_NAMEGRAFT_COPY","winbase/COPYFILE2_PHASE_NONE","winbase/COPYFILE2_PHASE_PREPARE_DEST","winbase/COPYFILE2_PHASE_PREPARE_SOURCE","winbase/COPYFILE2_PHASE_READ_SOURCE","winbase/COPYFILE2_PHASE_SERVER_COPY","winbase/COPYFILE2_PHASE_WRITE_DESTINATION"]
old-location: fs\copyfile2_copy_phase.htm
tech.root: fs
ms.assetid: 92bf9028-78a3-4ea3-bfbb-b53a8df557ab
ms.date: 12/05/2018
ms.keywords: COPYFILE2_COPY_PHASE, COPYFILE2_COPY_PHASE enumeration [Files], COPYFILE2_PHASE_MAX, COPYFILE2_PHASE_NAMEGRAFT_COPY, COPYFILE2_PHASE_NONE, COPYFILE2_PHASE_PREPARE_DEST, COPYFILE2_PHASE_PREPARE_SOURCE, COPYFILE2_PHASE_READ_SOURCE, COPYFILE2_PHASE_SERVER_COPY, COPYFILE2_PHASE_WRITE_DESTINATION, fs.copyfile2_copy_phase, winbase/COPYFILE2_COPY_PHASE, winbase/COPYFILE2_PHASE_MAX, winbase/COPYFILE2_PHASE_NAMEGRAFT_COPY, winbase/COPYFILE2_PHASE_NONE, winbase/COPYFILE2_PHASE_PREPARE_DEST, winbase/COPYFILE2_PHASE_PREPARE_SOURCE, winbase/COPYFILE2_PHASE_READ_SOURCE, winbase/COPYFILE2_PHASE_SERVER_COPY, winbase/COPYFILE2_PHASE_WRITE_DESTINATION
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
req.typenames: COPYFILE2_COPY_PHASE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COPYFILE2_COPY_PHASE
 - winbase/_COPYFILE2_COPY_PHASE
 - COPYFILE2_COPY_PHASE
 - winbase/COPYFILE2_COPY_PHASE
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
 - COPYFILE2_COPY_PHASE
---

# COPYFILE2_COPY_PHASE enumeration


## -description

Indicates the phase of a copy at the time of an error. This is used in the 
    <b>Error</b> structure embedded in the 
    <a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_message">COPYFILE2_MESSAGE</a> structure.

## -enum-fields

### -field COPYFILE2_PHASE_NONE:0

The copy had not yet started processing.

### -field COPYFILE2_PHASE_PREPARE_SOURCE

The source was being prepared including opening a handle to the source. This phase happens once per stream 
      copy operation.

### -field COPYFILE2_PHASE_PREPARE_DEST

The destination was being prepared including opening a handle to the destination. This phase happens once 
      per stream copy operation.

### -field COPYFILE2_PHASE_READ_SOURCE

The source file was being read. This phase happens one or more times per stream copy operation.

### -field COPYFILE2_PHASE_WRITE_DESTINATION

The destination file was being written. This phase happens one or more times per stream copy 
      operation.

### -field COPYFILE2_PHASE_SERVER_COPY

Both the source and destination were on the same remote server and the copy was being processed remotely. 
      This phase happens once per stream copy operation.

### -field COPYFILE2_PHASE_NAMEGRAFT_COPY

The copy operation was processing symbolic links and/or reparse points. This phase happens once per file 
      copy operation.

### -field COPYFILE2_PHASE_MAX

One greater than the maximum value. Valid values for this enumeration will be less than this value.

## -remarks

To compile an application that uses this enumeration, define the <b>_WIN32_WINNT</b> 
    macro as 0x0601 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-copyfile2_message">COPYFILE2_MESSAGE</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a>



<a href="/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>
