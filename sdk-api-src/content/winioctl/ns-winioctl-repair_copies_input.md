---
UID: NS:winioctl._REPAIR_COPIES_INPUT
title: REPAIR_COPIES_INPUT
description: Input structure for the FSCTL_REPAIR_COPIES control code.
helpviewer_keywords: ["*PREPAIR_COPIES_INPUT","PREPAIR_COPIES_INPUT","PREPAIR_COPIES_INPUT structure pointer [Files]","REPAIR_COPIES_INPUT","REPAIR_COPIES_INPUT structure [Files]","fs.repair_copies_input","winioctl/PREPAIR_COPIES_INPUT","winioctl/REPAIR_COPIES_INPUT"]
old-location: fs\repair_copies_input.htm
tech.root: fs
ms.assetid: c3cefb13-4825-4482-a87c-4ba482d3820b
ms.date: 12/05/2018
ms.keywords: '*PREPAIR_COPIES_INPUT, PREPAIR_COPIES_INPUT, PREPAIR_COPIES_INPUT structure pointer [Files], REPAIR_COPIES_INPUT, REPAIR_COPIES_INPUT structure [Files], fs.repair_copies_input, winioctl/PREPAIR_COPIES_INPUT, winioctl/REPAIR_COPIES_INPUT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: REPAIR_COPIES_INPUT, *PREPAIR_COPIES_INPUT
req.redist: 
f1_keywords:
 - _REPAIR_COPIES_INPUT
 - winioctl/_REPAIR_COPIES_INPUT
 - PREPAIR_COPIES_INPUT
 - winioctl/PREPAIR_COPIES_INPUT
 - REPAIR_COPIES_INPUT
 - winioctl/REPAIR_COPIES_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - REPAIR_COPIES_INPUT
---

# REPAIR_COPIES_INPUT structure


## -description

Input structure for the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_repair_copies">FSCTL_REPAIR_COPIES</a> control code. It describes a single block of data and indicates which of the copies is to be copied to the specified copies of the data. The

## -struct-fields

### -field Size

Set to <code>sizeof(REPAIR_COPIES_INPUT)</code>.

### -field Flags

Reserved (must be zero)

### -field FileOffset

The file position to start the repair operation.

### -field Length

The number of bytes to be repaired.

### -field SourceCopy

The zero-based copy number of the source copy.

### -field NumberOfRepairCopies

The number of copies that will be repaired. This is the size of the <b>RepairCopies</b> 
      array.

### -field RepairCopies

The zero-based copy numbers of the copies that will be repaired.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_repair_copies">FSCTL_REPAIR_COPIES</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-repair_copies_output">REPAIR_COPIES_OUTPUT</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>