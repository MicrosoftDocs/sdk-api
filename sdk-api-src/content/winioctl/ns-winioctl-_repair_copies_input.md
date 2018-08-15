---
UID: NS:winioctl._REPAIR_COPIES_INPUT
title: "_REPAIR_COPIES_INPUT"
author: windows-sdk-content
description: Input structure for the FSCTL_REPAIR_COPIES control code.
old-location: fs\repair_copies_input.htm
old-project: fileio
ms.assetid: c3cefb13-4825-4482-a87c-4ba482d3820b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PREPAIR_COPIES_INPUT, PREPAIR_COPIES_INPUT, PREPAIR_COPIES_INPUT structure pointer [Files], REPAIR_COPIES_INPUT, REPAIR_COPIES_INPUT structure [Files], _REPAIR_COPIES_INPUT, fs.repair_copies_input, winioctl/PREPAIR_COPIES_INPUT, winioctl/REPAIR_COPIES_INPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: REPAIR_COPIES_INPUT, *PREPAIR_COPIES_INPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - REPAIR_COPIES_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _REPAIR_COPIES_INPUT structure


## -description


Input structure for the <a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a> control code. It describes a single block of data and indicates which of the copies is to be copied to the specified copies of the data. The 


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




<a href="https://msdn.microsoft.com/1970ed09-5f37-4cc9-98c5-982629676fe4">FSCTL_REPAIR_COPIES</a>



<a href="https://msdn.microsoft.com/a3da7779-92e7-40bf-a889-dd2013e942ab">REPAIR_COPIES_OUTPUT</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

