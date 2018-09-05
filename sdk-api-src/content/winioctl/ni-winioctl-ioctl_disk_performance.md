---
UID: NI:winioctl.IOCTL_DISK_PERFORMANCE
title: IOCTL_DISK_PERFORMANCE
author: windows-sdk-content
description: Enables performance counters that provide disk performance information.
old-location: fs\ioctl_disk_performance.htm
old-project: fileio
ms.assetid: e182282c-17e9-442a-8742-437052cfed03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCTL_DISK_PERFORMANCE, IOCTL_DISK_PERFORMANCE control, IOCTL_DISK_PERFORMANCE control code [Files], _win32_ioctl_disk_performance, base.ioctl_disk_performance, fs.ioctl_disk_performance, winioctl/IOCTL_DISK_PERFORMANCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: WRITE_THROUGH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_DISK_PERFORMANCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_PERFORMANCE IOCTL


## -description


Enables performance counters that provide disk performance information.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



To disable the  performance counters enabled by this control code, use the <a href="https://msdn.microsoft.com/68f4f6fb-a4f3-4fa5-8187-b2287a4271e8">IOCTL_DISK_PERFORMANCE_OFF</a> control code.




## -see-also




<a href="https://msdn.microsoft.com/938ec37b-450e-4ebf-ad2b-9f1ac5f56112">DISK_PERFORMANCE</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/68f4f6fb-a4f3-4fa5-8187-b2287a4271e8">IOCTL_DISK_PERFORMANCE_OFF</a>
 

 

