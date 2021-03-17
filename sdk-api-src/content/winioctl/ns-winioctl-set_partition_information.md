---
UID: NS:winioctl._SET_PARTITION_INFORMATION
title: SET_PARTITION_INFORMATION
description: Contains information used to set a disk partition's type.
helpviewer_keywords: ["*PSET_PARTITION_INFORMATION","PSET_PARTITION_INFORMATION","PSET_PARTITION_INFORMATION structure pointer [Files]","SET_PARTITION_INFORMATION","SET_PARTITION_INFORMATION structure [Files]","SET_PARTITION_INFORMATION_MBR","_win32_set_partition_information_str","base.set_partition_information_str","fs.set_partition_information_str","winioctl/PSET_PARTITION_INFORMATION","winioctl/SET_PARTITION_INFORMATION"]
old-location: fs\set_partition_information_str.htm
tech.root: fs
ms.assetid: cc04868c-cb9c-455f-a0df-bde6a133eb60
ms.date: 12/05/2018
ms.keywords: '*PSET_PARTITION_INFORMATION, PSET_PARTITION_INFORMATION, PSET_PARTITION_INFORMATION structure pointer [Files], SET_PARTITION_INFORMATION, SET_PARTITION_INFORMATION structure [Files], SET_PARTITION_INFORMATION_MBR, _win32_set_partition_information_str, base.set_partition_information_str, fs.set_partition_information_str, winioctl/PSET_PARTITION_INFORMATION, winioctl/SET_PARTITION_INFORMATION'
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
targetos: Windows
req.typenames: SET_PARTITION_INFORMATION, *PSET_PARTITION_INFORMATION
req.redist: 
f1_keywords:
 - _SET_PARTITION_INFORMATION
 - winioctl/_SET_PARTITION_INFORMATION
 - PSET_PARTITION_INFORMATION
 - winioctl/PSET_PARTITION_INFORMATION
 - SET_PARTITION_INFORMATION
 - winioctl/SET_PARTITION_INFORMATION
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
 - SET_PARTITION_INFORMATION
---

# SET_PARTITION_INFORMATION structure


## -description

Contains information used to set a disk partition's type.
<div class="alert"><b>Note</b>  <b>SET_PARTITION_INFORMATION</b> has been superseded by the 
<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a> structure.</div><div> </div>

## -struct-fields

### -field PartitionType

The type of partition. For a list of values, see 
<a href="/windows/desktop/FileIO/disk-partition-types">Disk Partition Types</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info">IOCTL_DISK_GET_PARTITION_INFO</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info">IOCTL_DISK_SET_PARTITION_INFO</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a>