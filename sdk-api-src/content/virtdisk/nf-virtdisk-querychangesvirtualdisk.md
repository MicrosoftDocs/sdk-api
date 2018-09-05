---
UID: NF:virtdisk.QueryChangesVirtualDisk
title: QueryChangesVirtualDisk function
author: windows-sdk-content
description: Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).
old-location: vhd\querychangesvirtualdisk.htm
old-project: VStor
ms.assetid: 633FA684-5CC6-4615-B62C-54C60B38E652
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: QueryChangesVirtualDisk, QueryChangesVirtualDisk function [VHD], vdssys/QueryChangesVirtualDisk, vhd.querychangesvirtualdisk, virtdisk/QueryChangesVirtualDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: virtdisk.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - QueryChangesVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# QueryChangesVirtualDisk function


## -description


Retrieves information about changes  to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open VHD, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag set in the 
      <i>VirtualDiskAccessMask</i> parameter to the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function. For information on how to 
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

An array of <a href="https://msdn.microsoft.com/9DA53F46-AE1E-425B-BA50-05DC4A327F75">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a> structures that indicates the areas of the virtual disk within the area that the <i>ByteOffset</i> and <i>ByteLength</i> parameters specify that have changed since the change tracking identifier that the <i>ChangeTrackingId</i>  parameter specifies was sealed.


### -param RangeCount [in, out]

An address of an unsigned long integer. On input, the value indicates the number of <a href="https://msdn.microsoft.com/9DA53F46-AE1E-425B-BA50-05DC4A327F75">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a> structures that the array that the <i>Ranges</i> parameter points to can hold. On output, the value contains the number of <b>QUERY_CHANGES_VIRTUAL_DISK_RANGE</b> structures that the method placed in the array.


### -param ProcessedLength [out]

A pointer to an unsigned long integer that indicates the total number of bytes that the method processed, which indicates for how much of the area that the <i>BytesLength</i> parameter specifies that changes were captured in the available space of the array that the <i>Ranges</i> parameter specifies. 


## -returns



The status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <i>Ranges</i> parameter contains the requested information.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/9DA53F46-AE1E-425B-BA50-05DC4A327F75">QUERY_CHANGES_VIRTUAL_DISK_RANGE</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

