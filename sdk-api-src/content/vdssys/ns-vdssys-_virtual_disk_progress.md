---
UID: NS:vdssys._VIRTUAL_DISK_PROGRESS
title: "_VIRTUAL_DISK_PROGRESS"
author: windows-sdk-content
description: Contains the progress and result data for the current virtual hard disk (VHD) operation, used by the GetVirtualDiskOperationProgress function.
old-location: vhd\virtual_disk_progress.htm
old-project: VStor
ms.assetid: 834d7384-09fe-493e-8402-135c453a1ecf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PVIRTUAL_DISK_PROGRESS, PVIRTUAL_DISK_PROGRESS, PVIRTUAL_DISK_PROGRESS structure pointer [VHD], VIRTUAL_DISK_PROGRESS, VIRTUAL_DISK_PROGRESS structure [VHD], _VIRTUAL_DISK_PROGRESS, vdssys/PVIRTUAL_DISK_PROGRESS, vdssys/VIRTUAL_DISK_PROGRESS, vhd.virtual_disk_progress, virtdisk/PVIRTUAL_DISK_PROGRESS, virtdisk/VIRTUAL_DISK_PROGRESS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdssys.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: VIRTUAL_DISK_PROGRESS, *PVIRTUAL_DISK_PROGRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - VIRTUAL_DISK_PROGRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VIRTUAL_DISK_PROGRESS structure


## -description


Contains the progress and result data for the current virtual hard disk (VHD) operation, used by the 
    <a href="https://msdn.microsoft.com/392a5258-306d-4c06-a632-85e6fc65ddc9">GetVirtualDiskOperationProgress</a> 
    function.


## -struct-fields




### -field OperationStatus

A <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> status value, this member will 
     be <b>ERROR_IO_PENDING</b> if the operation is still in progress; otherwise, the value is the 
     result code of the completed operation.


### -field CurrentValue

The current progress of the operation, used in conjunction with the 
      <b>CompletionValue</b> member.

This value is meaningful only if 
     <b>OperationStatus</b> is <b>ERROR_IO_PENDING</b>.


### -field CompletionValue

The value that the <b>CurrentValue</b> member would be if the operation were complete.

This value is meaningful only if <b>OperationStatus</b> is 
      <b>ERROR_IO_PENDING</b>.


## -remarks



The <b>CurrentValue</b> and <b>CompletionValue</b> members are 
    intended to be used for calculating a percentage value, and the specific numeric values of each are not 
    significant in any way. Only the result of the following calculation is meaningful: 
    <b>CurrentValue</b> divided by <b>CompletionValue</b> multiplied by 100 
    equals percent complete, up to and including 100 percent, even when <b>OperationStatus</b> is 
    still returning <b>ERROR_IO_PENDING</b>. This percentage is not always guaranteed to increase 
    with subsequent calls to the 
    <a href="https://msdn.microsoft.com/392a5258-306d-4c06-a632-85e6fc65ddc9">GetVirtualDiskOperationProgress</a> 
    function, and may decrease. These decreased percentages may be safely ignored if progress tracking is desired to 
    be only in the positive by locally storing the current maximum percentage.

The <b>CurrentValue</b> and <b>CompletionValue</b> members can vary in 
    subsequent calls to the 
    <a href="https://msdn.microsoft.com/392a5258-306d-4c06-a632-85e6fc65ddc9">GetVirtualDiskOperationProgress</a> 
    function, so they must be used together at the same time from the same call. That is, it is not valid to save 
    either of them locally and then make another call to the 
    <b>GetVirtualDiskOperationProgress</b> 
    function expecting to use either of the previous values with the other value from the more recent call.

The <b>OperationStatus</b> member is the indicator of completion, not the percent-complete 
    calculation described previously. As long as this data member is returning with an 
    <b>ERROR_IO_PENDING</b> status code, the I/O operation is not yet complete.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/392a5258-306d-4c06-a632-85e6fc65ddc9">GetVirtualDiskOperationProgress</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

