---
UID: NI:winioctl.IOCTL_DISK_PERFORMANCE_OFF
title: IOCTL_DISK_PERFORMANCE_OFF
description: Disables the performance counters that provide disk performance information.
old-location: fs\ioctl_disk_performance_off.htm
tech.root: FileIO
ms.assetid: 68f4f6fb-a4f3-4fa5-8187-b2287a4271e8
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_PERFORMANCE_OFF, IOCTL_DISK_PERFORMANCE_OFF control, IOCTL_DISK_PERFORMANCE_OFF control code [Files], base.ioctl_disk_performance_off, fs.ioctl_disk_performance_off, winioctl/IOCTL_DISK_PERFORMANCE_OFF
f1_keywords:
- winioctl/IOCTL_DISK_PERFORMANCE_OFF
dev_langs:
- c++
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
- IOCTL_DISK_PERFORMANCE_OFF
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_PERFORMANCE_OFF IOCTL


## -description


Disables the performance counters that provide disk performance information.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_PERFORMANCE_OFF,  // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSizeNULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
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



To enable these performance counters, use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance">IOCTL_DISK_PERFORMANCE</a> control code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk
		  Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance">IOCTL_DISK_PERFORMANCE</a>
 

 

