---
UID: NS:virtdisk._QUERY_CHANGES_VIRTUAL_DISK_RANGE
title: QUERY_CHANGES_VIRTUAL_DISK_RANGE
author: windows-sdk-content
description: Identifies an area on a virtual hard disk (VHD) that has changed as tracked by resilient change tracking (RCT).
old-location: vhd\query_changes_virtual_disk_range.htm
tech.root: VStor
ms.assetid: 9DA53F46-AE1E-425B-BA50-05DC4A327F75
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PQUERY_CHANGES_VIRTUAL_DISK_RANGE, PQUERY_CHANGES_VIRTUAL_DISK_RANGE, PQUERY_CHANGES_VIRTUAL_DISK_RANGE structure pointer [VHD], QUERY_CHANGES_VIRTUAL_DISK_RANGE, QUERY_CHANGES_VIRTUAL_DISK_RANGE structure [VHD], __QUERY_CHANGES_VIRTUAL_DISK_RANGE, vdssys/PQUERY_CHANGES_VIRTUAL_DISK_RANGE, vdssys/QUERY_CHANGES_VIRTUAL_DISK_RANGE, vhd.query_changes_virtual_disk_range, virtdisk/PQUERY_CHANGES_VIRTUAL_DISK_RANGE, virtdisk/QUERY_CHANGES_VIRTUAL_DISK_RANGE"
ms.topic: struct
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
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
 - VirtDisk.h
 - vdssys.h
api_name:
 - QUERY_CHANGES_VIRTUAL_DISK_RANGE
product: Windows
targetos: Windows
req.typenames: QUERY_CHANGES_VIRTUAL_DISK_RANGE, *PQUERY_CHANGES_VIRTUAL_DISK_RANGE
req.redist: 
---

# QUERY_CHANGES_VIRTUAL_DISK_RANGE structure


## -description


Identifies an area on a virtual hard disk (VHD) that has changed as tracked by resilient change tracking (RCT).


## -struct-fields




### -field ByteOffset

The distance from the start of the virtual disk to the beginning of  the area of the virtual disk that has changed, in bytes.


### -field ByteLength

The length of the area of the virtual disk that has changed, in bytes.


### -field Reserved

Reserved. 


## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt162230(v=VS.85).aspx">QueryCangesVirtualDisk</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

