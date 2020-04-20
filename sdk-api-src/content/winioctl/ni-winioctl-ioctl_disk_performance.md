---
UID: NI:winioctl.IOCTL_DISK_PERFORMANCE
title: IOCTL_DISK_PERFORMANCE
description: Enables performance counters that provide disk performance information.helpviewer_keywords: ["IOCTL_DISK_PERFORMANCE","IOCTL_DISK_PERFORMANCE control","IOCTL_DISK_PERFORMANCE control code [Files]","_win32_ioctl_disk_performance","base.ioctl_disk_performance","fs.ioctl_disk_performance","winioctl/IOCTL_DISK_PERFORMANCE"]
old-location: fs\ioctl_disk_performance.htm
tech.root: FileIO
ms.assetid: e182282c-17e9-442a-8742-437052cfed03
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_PERFORMANCE, IOCTL_DISK_PERFORMANCE control, IOCTL_DISK_PERFORMANCE control code [Files], _win32_ioctl_disk_performance, base.ioctl_disk_performance, fs.ioctl_disk_performance, winioctl/IOCTL_DISK_PERFORMANCE
f1_keywords:
- winioctl/IOCTL_DISK_PERFORMANCE
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
- IOCTL_DISK_PERFORMANCE
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_PERFORMANCE IOCTL


## -description


Enables performance counters that provide disk performance information.

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
  IOCTL_DISK_PERFORMANCE,      // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSize(LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



To disable the  performance counters enabled by this control code, use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance_off">IOCTL_DISK_PERFORMANCE_OFF</a> control code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_performance">DISK_PERFORMANCE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_performance_off">IOCTL_DISK_PERFORMANCE_OFF</a>
 

 

