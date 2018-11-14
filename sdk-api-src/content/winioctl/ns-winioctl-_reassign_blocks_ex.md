---
UID: NS:winioctl._REASSIGN_BLOCKS_EX
title: "_REASSIGN_BLOCKS_EX"
author: windows-sdk-content
description: Contains disk block reassignment data.
old-location: fs\reassign_blocks_ex.htm
tech.root: fileio
ms.assetid: 48036bdc-3588-41a6-9dbb-4606bdfcb683
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PREASSIGN_BLOCKS_EX, PREASSIGN_BLOCKS_EX, PREASSIGN_BLOCKS_EX structure pointer [Files], REASSIGN_BLOCKS_EX, REASSIGN_BLOCKS_EX structure [Files], _REASSIGN_BLOCKS_EX, base.reassign_blocks_ex, fs.reassign_blocks_ex, winioctl/PREASSIGN_BLOCKS_EX, winioctl/REASSIGN_BLOCKS_EX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - REASSIGN_BLOCKS_EX
product: Windows
targetos: Windows
req.typenames: REASSIGN_BLOCKS_EX, *PREASSIGN_BLOCKS_EX
req.redist: 
---

# _REASSIGN_BLOCKS_EX structure


## -description


Contains 
    disk block reassignment data. This is a variable length structure where the last member is an array of block 
    numbers to be reassigned. It is used by the 
    <a href="https://msdn.microsoft.com/126ffefa-165b-4ca1-a905-1aebc8e790c7">IOCTL_DISK_REASSIGN_BLOCKS_EX</a> control 
    code.


## -struct-fields




### -field Reserved

This member is reserved. Do not use it. Set it to 0 (zero).


### -field Count

The number of blocks to be reassigned. 

This is the number of elements that are in the 
      <b>BlockNumber</b> member array.


### -field BlockNumber

An array of <b>Count</b> block numbers, one for each block to be reassigned.


## -remarks



The <b>REASSIGN_BLOCKS_EX</b> structure supports drives 
    that have an 8-byte Logical Block Address (LBA), which is typically required for storage devices larger than 2 TB. 
    The <a href="https://msdn.microsoft.com/43d908fc-0e43-49ab-a96f-b6b0f491c99d">REASSIGN_BLOCKS</a> structure used with the 
    <a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a> control code 
    supports devices with up to a 4-byte LBA should be used where possible.




## -see-also




<a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a>



<a href="https://msdn.microsoft.com/126ffefa-165b-4ca1-a905-1aebc8e790c7">IOCTL_DISK_REASSIGN_BLOCKS_EX</a>



<a href="https://msdn.microsoft.com/43d908fc-0e43-49ab-a96f-b6b0f491c99d">REASSIGN_BLOCKS</a>
 

 

