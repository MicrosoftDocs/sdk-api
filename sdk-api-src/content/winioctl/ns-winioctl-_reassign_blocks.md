---
UID: NS:winioctl._REASSIGN_BLOCKS
title: "_REASSIGN_BLOCKS"
author: windows-sdk-content
description: Contains disk block reassignment data.
old-location: fs\reassign_blocks_str.htm
tech.root: fileio
ms.assetid: 43d908fc-0e43-49ab-a96f-b6b0f491c99d
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PREASSIGN_BLOCKS, REASSIGN_BLOCKS, REASSIGN_BLOCKS structure [Files], _REASSIGN_BLOCKS, _win32_reassign_blocks_str, base.reassign_blocks_str, fs.reassign_blocks_str, winioctl/REASSIGN_BLOCKS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - REASSIGN_BLOCKS
product: Windows
targetos: Windows
req.typenames: REASSIGN_BLOCKS, *PREASSIGN_BLOCKS
req.redist: 
---

# _REASSIGN_BLOCKS structure


## -description


Contains 
    disk block reassignment data. This is a variable length structure where the last member is an array of block 
    numbers to be reassigned. It is used by the 
    <a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a> control code.


## -struct-fields




### -field Reserved

This member is reserved. Do not use it. Set it to zero.


### -field Count

The number of blocks to be reassigned. 

This is the number of elements that are in the 
      <b>BlockNumber</b> member array.


### -field BlockNumber

An array of <b>Count</b> block numbers, one for each block to be reassigned.


## -remarks



The <b>REASSIGN_BLOCKS</b> structure only supports 
    drives where the Logical Block Address (LBA) is a 4-byte value (typically up to 2 TB). 

For larger drives the 
    <a href="https://msdn.microsoft.com/48036bdc-3588-41a6-9dbb-4606bdfcb683">REASSIGN_BLOCKS_EX</a> structure that is  used with the 
    <a href="https://msdn.microsoft.com/126ffefa-165b-4ca1-a905-1aebc8e790c7">IOCTL_DISK_REASSIGN_BLOCKS_EX</a> control code 
    supports 8-byte LBAs.

For device compatibility, the 
    <a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a> control code and 
    <b>REASSIGN_BLOCKS</b> structure should be used where 
    possible.




## -see-also




<a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a>



<a href="https://msdn.microsoft.com/126ffefa-165b-4ca1-a905-1aebc8e790c7">IOCTL_DISK_REASSIGN_BLOCKS_EX</a>



<a href="https://msdn.microsoft.com/48036bdc-3588-41a6-9dbb-4606bdfcb683">REASSIGN_BLOCKS_EX</a>
 

 

