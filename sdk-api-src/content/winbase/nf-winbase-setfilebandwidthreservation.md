---
UID: NF:winbase.SetFileBandwidthReservation
title: SetFileBandwidthReservation function (winbase.h)
description: Requests that bandwidth for the specified file stream be reserved. The reservation is specified as a number of bytes in a period of milliseconds for I/O requests on the specified file handle.
helpviewer_keywords: ["SetFileBandwidthReservation","SetFileBandwidthReservation function [Files]","fs.setfilebandwidthreservation_func","winbase/SetFileBandwidthReservation"]
old-location: fs\setfilebandwidthreservation_func.htm
tech.root: fs
ms.assetid: a22bd8f3-4fbf-4f77-b8b6-7e786942615a
ms.date: 12/05/2018
ms.keywords: SetFileBandwidthReservation, SetFileBandwidthReservation function [Files], fs.setfilebandwidthreservation_func, winbase/SetFileBandwidthReservation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetFileBandwidthReservation
 - winbase/SetFileBandwidthReservation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - SetFileBandwidthReservation
---

# SetFileBandwidthReservation function


## -description

Requests that bandwidth for the specified file stream be reserved. The reservation is specified as a 
    number of bytes in a period of milliseconds for I/O requests on the specified  file handle.

## -parameters

### -param hFile [in]

A handle to the file.

### -param nPeriodMilliseconds [in]

The period of the reservation, in milliseconds. The period is the time from which the I/O is issued to the 
      kernel until the time the I/O should be completed. The minimum supported value for the file 
      stream can be determined by looking at the value returned through the 
      <i>lpPeriodMilliseconds</i> parameter to the 
      <a href="/windows/desktop/api/winbase/nf-winbase-getfilebandwidthreservation">GetFileBandwidthReservation</a> function, 
      on a handle that has not had a bandwidth reservation set.

### -param nBytesPerPeriod [in]

The bandwidth to reserve, in bytes per period. The maximum supported value for the file 
      stream can be determined by looking at the value returned through the 
      <i>lpBytesPerPeriod</i> parameter to the 
      <a href="/windows/desktop/api/winbase/nf-winbase-getfilebandwidthreservation">GetFileBandwidthReservation</a> function, 
      on a handle that has not had a bandwidth reservation set.

### -param bDiscardable [in]

Indicates whether I/O should be completed with an error if a driver is unable to satisfy an I/O operation 
      before the period expires. If one of the drivers for the specified file stream does not support this 
      functionality, this function may return success and ignore the flag. To verify whether the setting will be 
      honored, call the 
      <a href="/windows/desktop/api/winbase/nf-winbase-getfilebandwidthreservation">GetFileBandwidthReservation</a> function 
      using the same <i>hFile</i> handle and examine the <i>*pDiscardable</i> 
      return value.

### -param lpTransferSize [out]

A pointer to a variable that receives the minimum size of any individual I/O request that may be issued by 
      the application. All I/O requests should be multiples of <i>TransferSize</i>.

### -param lpNumOutstandingRequests [out]

A pointer to a variable that receives the number of <i>TransferSize</i> chunks the 
      application should allow to be outstanding with the operating system. This allows the storage stack to keep the 
      device busy and allows maximum throughput.

## -returns

Returns nonzero if successful or zero otherwise.

A reservation can fail if there is not enough bandwidth available on the volume because of existing 
       reservations; in this case <b>ERROR_NO_SYSTEM_RESOURCES</b> is returned.

To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The requested bandwidth reservation must be greater than or equal to one packet per period. The minimum period, 
     in milliseconds, maximum bytes per period, and minimum transfer size, in bytes, for a specific volume are 
     returned through the <i>lpPeriodMilliseconds</i>, <i>lpBytesPerPeriod</i>, 
     and  <i>lpTransferSize</i> parameters to 
     <a href="/windows/desktop/api/winbase/nf-winbase-getfilebandwidthreservation">GetFileBandwidthReservation</a> on a 
     handle that has not been used in a call to 
     <b>SetFileBandwidthReservation</b>. In other 
     words: 

1 ≤ (<i>nBytesPerPeriod</i>)×(*<i>lpPeriodMilliseconds</i>)/(*<i>lpTransferSize</i>)/(<i>nPeriodMilliseconds</i>)

IIn Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfilebandwidthreservation">GetFileBandwidthReservation</a>