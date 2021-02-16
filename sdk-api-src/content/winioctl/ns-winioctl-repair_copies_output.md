---
UID: NS:winioctl._REPAIR_COPIES_OUTPUT
title: REPAIR_COPIES_OUTPUT
description: Contains output of a repair copies operation returned from the FSCTL_REPAIR_COPIES control code.
helpviewer_keywords: ["*PREPAIR_COPIES_OUTPUT","PREPAIR_COPIES_OUTPUT","PREPAIR_COPIES_OUTPUT structure pointer [Files]","REPAIR_COPIES_OUTPUT","REPAIR_COPIES_OUTPUT structure [Files]","fs.repair_copies_output","winioctl/PREPAIR_COPIES_OUTPUT","winioctl/REPAIR_COPIES_OUTPUT"]
old-location: fs\repair_copies_output.htm
tech.root: fs
ms.assetid: a3da7779-92e7-40bf-a889-dd2013e942ab
ms.date: 12/05/2018
ms.keywords: '*PREPAIR_COPIES_OUTPUT, PREPAIR_COPIES_OUTPUT, PREPAIR_COPIES_OUTPUT structure pointer [Files], REPAIR_COPIES_OUTPUT, REPAIR_COPIES_OUTPUT structure [Files], fs.repair_copies_output, winioctl/PREPAIR_COPIES_OUTPUT, winioctl/REPAIR_COPIES_OUTPUT'
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
req.typenames: REPAIR_COPIES_OUTPUT, *PREPAIR_COPIES_OUTPUT
req.redist: 
f1_keywords:
 - _REPAIR_COPIES_OUTPUT
 - winioctl/_REPAIR_COPIES_OUTPUT
 - PREPAIR_COPIES_OUTPUT
 - winioctl/PREPAIR_COPIES_OUTPUT
 - REPAIR_COPIES_OUTPUT
 - winioctl/REPAIR_COPIES_OUTPUT
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
 - REPAIR_COPIES_OUTPUT
---

# REPAIR_COPIES_OUTPUT structure


## -description

Contains output of a repair copies operation returned from the 
     <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_repair_copies">FSCTL_REPAIR_COPIES</a> control code.

## -struct-fields

### -field Size

Set to <code>sizeof(REPAIR_COPIES_OUTPUT)</code>.

### -field Status

Indicates the status of the repair operation. The value is a <b>NTSTATUS</b> value. 
      See 
      <a href="/openspecs/windows_protocols/ms-erref/596a1078-e883-4972-9bbc-49e60bebca55">http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx</a> 
      for a list of <b>NTSTATUS</b> values.

### -field ResumeFileOffset

If the <b>Status</b> member indicates the operation was not successful, this is the 
      file offset to use to resume repair operations, skipping the range where errors were found.