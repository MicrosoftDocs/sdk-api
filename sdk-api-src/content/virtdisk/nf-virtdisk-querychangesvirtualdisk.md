---
UID: NF:virtdisk.QueryChangesVirtualDisk
title: QueryChangesVirtualDisk function (virtdisk.h)
description: Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).
helpviewer_keywords: ["QueryChangesVirtualDisk","QueryChangesVirtualDisk function [VHD]","vdssys/QueryChangesVirtualDisk","vhd.querychangesvirtualdisk","virtdisk/QueryChangesVirtualDisk"]
old-location: vhd\querychangesvirtualdisk.htm
tech.root: VStor
ms.assetid: 633FA684-5CC6-4615-B62C-54C60B38E652
ms.date: 12/05/2018
ms.keywords: QueryChangesVirtualDisk, QueryChangesVirtualDisk function [VHD], vdssys/QueryChangesVirtualDisk, vhd.querychangesvirtualdisk, virtdisk/QueryChangesVirtualDisk
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryChangesVirtualDisk
 - virtdisk/QueryChangesVirtualDisk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - QueryChangesVirtualDisk
---

# QueryChangesVirtualDisk function


## -description

Retrieves information about changes  to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open VHD, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag set in the 
      <i>VirtualDiskAccessMask</i> parameter to the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function. For information on how to 
      open a VHD, see the <b>OpenVirtualDisk</b> function.

### -param ChangeTrackingId [in]

A pointer to a string that specifies the change tracking identifier for the change that identifies the state of the virtual disk that you want to use as the basis of comparison to determine whether the specified area of the VHD has changed.

### -param ByteOffset [in]

An unsigned long integer that specifies the distance from the start of the VHD to the beginning of  the area of the VHD that you want to check for changes, in bytes.

### -param ByteLength [in]

An unsigned long integer that specifies the length of the area of the VHD that you want to check for changes, in bytes.

### -param Flags [in]

Reserved. Set to <b>QUERY_CHANGES_VIRTUAL_DISK_FLAG_NONE</b>.

### -param Ranges [out]

An array of <a href="/windows/win32/api/virtdisk/ns-virtdisk-query_changes_virtual_disk_range">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a> structures that indicates the areas of the virtual disk within the area that the <i>ByteOffset</i> and <i>ByteLength</i> parameters specify that have changed since the change tracking identifier that the <i>ChangeTrackingId</i>  parameter specifies was sealed.

### -param RangeCount [in, out]

An address of an unsigned long integer. On input, the value indicates the number of <a href="/windows/win32/api/virtdisk/ns-virtdisk-query_changes_virtual_disk_range">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a> structures that the array that the <i>Ranges</i> parameter points to can hold. On output, the value contains the number of <b>QUERY_CHANGES_VIRTUAL_DISK_RANGE</b> structures that the method placed in the array.

### -param ProcessedLength [out]

A pointer to an unsigned long integer that indicates the total number of bytes that the method processed, which indicates for how much of the area that the <i>BytesLength</i> parameter specifies that changes were captured in the available space of the array that the <i>Ranges</i> parameter specifies.

## -returns

The status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <i>Ranges</i> parameter contains the requested information.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/ns-virtdisk-query_changes_virtual_disk_range">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>