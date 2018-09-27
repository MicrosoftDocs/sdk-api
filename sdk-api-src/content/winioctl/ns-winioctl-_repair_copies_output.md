---
UID: NS:winioctl._REPAIR_COPIES_OUTPUT
title: "_REPAIR_COPIES_OUTPUT"
author: windows-sdk-content
description: Contains output of a repair copies operation returned from the FSCTL_REPAIR_COPIES control code.
old-location: fs\repair_copies_output.htm
tech.root: fileio
ms.assetid: a3da7779-92e7-40bf-a889-dd2013e942ab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PREPAIR_COPIES_OUTPUT, PREPAIR_COPIES_OUTPUT, PREPAIR_COPIES_OUTPUT structure pointer [Files], REPAIR_COPIES_OUTPUT, REPAIR_COPIES_OUTPUT structure [Files], _REPAIR_COPIES_OUTPUT, fs.repair_copies_output, winioctl/PREPAIR_COPIES_OUTPUT, winioctl/REPAIR_COPIES_OUTPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - REPAIR_COPIES_OUTPUT
product: Windows
targetos: Windows
req.typenames: REPAIR_COPIES_OUTPUT, *PREPAIR_COPIES_OUTPUT
req.redist: 
---

# _REPAIR_COPIES_OUTPUT structure


## -description


Contains output of a repair copies operation returned from the 
     <a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a> control code.


## -struct-fields




### -field Size

Set to <code>sizeof(REPAIR_COPIES_OUTPUT)</code>.


### -field Status

Indicates the status of the repair operation. The value is a <b>NTSTATUS</b> value. 
      See 
      <a href="http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx">http://msdn.microsoft.com/en-us/library/cc704588(PROT.10).aspx</a> 
      for a list of <b>NTSTATUS</b> values.


### -field ResumeFileOffset

If the <b>Status</b> member indicates the operation was not successful, this is the 
      file offset to use to resume repair operations, skipping the range where errors were found.

