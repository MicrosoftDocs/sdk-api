---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOCTL_SERIAL_LSRMST_INSERT IOCTL


## -description


Enables or disables the placement of line status and modem status values into the regular data stream that an application acquires through the 
<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> function.

When this line-status and modem-status data placement mode is enabled, status values are preceded in the data stream by an escape character. The user-definable escape character is set by the 
<b>IOCTL_SERIAL_LSRMST_INSERT</b> control code. See the Remarks section for status value details.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_SERIAL_LSRMST_INSERT,  // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);</pre>
</td>
</tr>
</table></span></div>

## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



<div class="alert"><b>Note</b>  An application that uses this scheme must examine each character in the data stream to determine the presence of modem-status or line-status data.</div>
<div> </div>
The following values follow the designated escape character in the data stream if the <b>LSRMST_INSERT</b> mode has been turned on.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>SERIAL_LSRMST_ESCAPE</b></td>
<td>Indicates the reception of the escape character itself into the data stream.</td>
</tr>
<tr>
<td><b>SERIAL_LSRMST_LSR_DATA</b></td>
<td>Indicates that a line status change occurred, and data was available in the receive hardware buffer. Following this <b>BYTE</b> is a <b>BYTE</b> value of the line status register is the <b>BYTE</b> present in the receive hardware buffer when the line status change was processed.</td>
</tr>
<tr>
<td><b>SERIAL_LSRMST_LSR_NODATA</b></td>
<td>Indicates that a line status change occurred, but no data was available in the receive hardware buffer.</td>
</tr>
<tr>
<td><b>SERIAL_LSRMST_MST</b></td>
<td>Indicates that a modem status change occurred. Following this <b>BYTE</b> is a <b>BYTE</b> that is the value of the modem status register when the modem status change was processed.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

