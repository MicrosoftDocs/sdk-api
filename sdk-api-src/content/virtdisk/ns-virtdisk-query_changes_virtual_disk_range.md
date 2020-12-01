---
UID: NS:virtdisk._QUERY_CHANGES_VIRTUAL_DISK_RANGE
title: QUERY_CHANGES_VIRTUAL_DISK_RANGE (virtdisk.h)
description: Identifies an area on a virtual hard disk (VHD) that has changed as tracked by resilient change tracking (RCT).
helpviewer_keywords: ["*PQUERY_CHANGES_VIRTUAL_DISK_RANGE","PQUERY_CHANGES_VIRTUAL_DISK_RANGE","PQUERY_CHANGES_VIRTUAL_DISK_RANGE structure pointer [VHD]","QUERY_CHANGES_VIRTUAL_DISK_RANGE","QUERY_CHANGES_VIRTUAL_DISK_RANGE structure [VHD]","__QUERY_CHANGES_VIRTUAL_DISK_RANGE","vdssys/PQUERY_CHANGES_VIRTUAL_DISK_RANGE","vdssys/QUERY_CHANGES_VIRTUAL_DISK_RANGE","vhd.query_changes_virtual_disk_range","virtdisk/PQUERY_CHANGES_VIRTUAL_DISK_RANGE","virtdisk/QUERY_CHANGES_VIRTUAL_DISK_RANGE"]
old-location: vhd\query_changes_virtual_disk_range.htm
tech.root: VStor
ms.assetid: 9DA53F46-AE1E-425B-BA50-05DC4A327F75
ms.date: 12/05/2018
ms.keywords: '*PQUERY_CHANGES_VIRTUAL_DISK_RANGE, PQUERY_CHANGES_VIRTUAL_DISK_RANGE, PQUERY_CHANGES_VIRTUAL_DISK_RANGE structure pointer [VHD], QUERY_CHANGES_VIRTUAL_DISK_RANGE, QUERY_CHANGES_VIRTUAL_DISK_RANGE structure [VHD], __QUERY_CHANGES_VIRTUAL_DISK_RANGE, vdssys/PQUERY_CHANGES_VIRTUAL_DISK_RANGE, vdssys/QUERY_CHANGES_VIRTUAL_DISK_RANGE, vhd.query_changes_virtual_disk_range, virtdisk/PQUERY_CHANGES_VIRTUAL_DISK_RANGE, virtdisk/QUERY_CHANGES_VIRTUAL_DISK_RANGE'
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
targetos: Windows
req.typenames: QUERY_CHANGES_VIRTUAL_DISK_RANGE, *PQUERY_CHANGES_VIRTUAL_DISK_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QUERY_CHANGES_VIRTUAL_DISK_RANGE
 - virtdisk/_QUERY_CHANGES_VIRTUAL_DISK_RANGE
 - PQUERY_CHANGES_VIRTUAL_DISK_RANGE
 - virtdisk/PQUERY_CHANGES_VIRTUAL_DISK_RANGE
 - QUERY_CHANGES_VIRTUAL_DISK_RANGE
 - virtdisk/QUERY_CHANGES_VIRTUAL_DISK_RANGE
dev_langs:
 - c++
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

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



[QueryChangesVirtualDisk](./nf-virtdisk-querychangesvirtualdisk.md)



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>