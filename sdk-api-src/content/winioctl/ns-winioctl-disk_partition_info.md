---
UID: NS:winioctl._DISK_PARTITION_INFO
title: DISK_PARTITION_INFO
author: windows-sdk-content
description: Contains the disk partition information.
old-location: fs\disk_partition_info_str.htm
tech.root: FileIO
ms.assetid: 34a086fc-72ea-46ed-adb3-c084abcb3c74
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDISK_PARTITION_INFO, DISK_PARTITION_INFO, DISK_PARTITION_INFO structure [Files], PDISK_PARTITION_INFO, PDISK_PARTITION_INFO structure pointer [Files], _win32_disk_partition_info_str, base.disk_partition_info_str, fs.disk_partition_info_str, winioctl/DISK_PARTITION_INFO, winioctl/PDISK_PARTITION_INFO"
ms.topic: struct
f1_keywords: 
 - "winioctl/DISK_PARTITION_INFO"
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
 - DISK_PARTITION_INFO
product: Windows
targetos: Windows
req.typenames: DISK_PARTITION_INFO, *PDISK_PARTITION_INFO
req.redist: 
---

# DISK_PARTITION_INFO structure


## -description


Contains the disk partition information.


## -struct-fields




### -field SizeOfPartitionInfo

The size of this structure, in bytes.


### -field PartitionStyle

The format of a partition.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-_partition_style">PARTITION_STYLE</a>.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Mbr

If <b>PartitionStyle</b> is <b>PARTITION_STYLE_MBR</b> (0), the union 
        is a structure that contains information for an master boot record partition, which includes a disk signature 
        and a checksum.


### -field DUMMYUNIONNAME.Mbr.Signature

MBR signature of the partition.


### -field DUMMYUNIONNAME.Mbr.CheckSum

 


### -field DUMMYUNIONNAME.Gpt

If <b>PartitionStyle</b> is <b>PARTITION_STYLE_GPT</b> (1), the union 
        is a structure that contains information for a <b>GUID</b> partition table partition, 
        which includes a disk identifier (<b>GUID</b>).


### -field DUMMYUNIONNAME.Gpt.DiskId

<b>GUID</b> of the GPT partition.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_geometry_ex">DISK_GEOMETRY_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-_partition_style">PARTITION_STYLE</a>
 

 

