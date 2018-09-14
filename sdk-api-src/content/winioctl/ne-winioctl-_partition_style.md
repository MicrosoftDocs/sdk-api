---
UID: NE:winioctl._PARTITION_STYLE
title: "_PARTITION_STYLE"
author: windows-sdk-content
description: Represents the format of a partition.
old-location: fs\partition_style_str.htm
tech.root: FileIO
ms.assetid: 254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PARTITION_STYLE, PARTITION_STYLE enumeration [Files], PARTITION_STYLE_GPT, PARTITION_STYLE_MBR, PARTITION_STYLE_RAW, _PARTITION_STYLE, _win32_partition_style_str, base.partition_style_str, fs.partition_style_str, winioctl/PARTITION_STYLE, winioctl/PARTITION_STYLE_GPT, winioctl/PARTITION_STYLE_MBR, winioctl/PARTITION_STYLE_RAW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winioctl.h
req.include-header: 
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
 - PARTITION_STYLE
product: Windows
targetos: Windows
req.typenames: PARTITION_STYLE
req.redist: 
---

# _PARTITION_STYLE enumeration


## -description


Represents the format of a partition.


## -enum-fields




### -field PARTITION_STYLE_MBR

Master boot record (MBR) format. This corresponds to standard <i>AT-style</i> MBR partitions.


### -field PARTITION_STYLE_GPT

GUID Partition Table (GPT) format.


### -field PARTITION_STYLE_RAW

Partition not formatted in either of the recognized formats—MBR or GPT.


## -see-also




<a href="https://msdn.microsoft.com/a5b1e97c-f22a-4d90-a3f4-1589ad9d1cc3">File System Recognition</a>



<a href="https://msdn.microsoft.com/f84f8be6-2b01-4a20-8669-cb1a55c32907">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/3c88ebae-274e-403a-8f57-58fdf863f511">PARTITION_INFORMATION_EX</a>
 

 

