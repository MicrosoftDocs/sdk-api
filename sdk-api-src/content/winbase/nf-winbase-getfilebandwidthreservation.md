---
UID: NF:winbase.GetFileBandwidthReservation
title: GetFileBandwidthReservation function
author: windows-sdk-content
description: Retrieves the bandwidth reservation properties of the volume on which the specified file resides.
old-location: fs\getfilebandwidthreservation_func.htm
tech.root: FileIO
ms.assetid: 3caf38f6-e853-4057-a192-71cda4443dbd
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetFileBandwidthReservation, GetFileBandwidthReservation function [Files], fs.getfilebandwidthreservation_func, winbase/GetFileBandwidthReservation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - GetFileBandwidthReservation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileBandwidthReservation function


## -description


Retrieves the bandwidth reservation properties of the volume on which the specified file resides.


## -parameters




### -param hFile [in]

A handle to the file.


### -param lpPeriodMilliseconds [out]

A pointer to a variable that receives the period of the reservation, in milliseconds. The period is the 
      time from which the I/O is issued to the kernel until the time the I/O should be completed. If no bandwidth has 
      been reserved for this handle, then the value returned is the minimum reservation period supported for this 
      volume.


### -param lpBytesPerPeriod [out]

A pointer to a variable that receives the maximum number of bytes per period that can be reserved on the 
      volume. If no bandwidth has been reserved for this handle, then the value returned is the maximum number of 
      bytes per period supported for the volume.


### -param pDiscardable [out]

<b>TRUE</b> if I/O should be completed with an error if a driver is unable to satisfy an 
      I/O operation before the period expires. <b>FALSE</b> if the underlying subsystem does not 
      support failing in this manner.


### -param lpTransferSize [out]

The minimum size of any individual I/O request that may be issued by the application. All I/O requests 
      should be multiples of <i>TransferSize</i>. If no bandwidth has been reserved for this 
      handle, then the value returned is the minimum transfer size supported for this volume.


### -param lpNumOutstandingRequests [out]

The number of <i>TransferSize</i> chunks  allowed to be outstanding with the operating 
      system.


## -returns



Returns nonzero if successful or zero otherwise.

To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/a22bd8f3-4fbf-4f77-b8b6-7e786942615a">SetFileBandwidthReservation</a>
 

 

