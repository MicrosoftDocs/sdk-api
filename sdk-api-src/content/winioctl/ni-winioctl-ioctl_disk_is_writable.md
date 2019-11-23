---
UID: NI:winioctl.IOCTL_DISK_IS_WRITABLE
title: IOCTL_DISK_IS_WRITABLE

description: Determines whether the specified disk is writable.
old-location: fs\ioctl_disk_is_writable.htm
tech.root: FileIO
ms.assetid: 0b56ea0d-95ae-4306-9866-b4b5e985ed43

ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_IS_WRITABLE, IOCTL_DISK_IS_WRITABLE control, IOCTL_DISK_IS_WRITABLE control code [Files], base.ioctl_disk_is_writable, fs.ioctl_disk_is_writable, winioctl/IOCTL_DISK_IS_WRITABLE
ms.topic: ioctl
f1_keywords: 
 - "winioctl/IOCTL_DISK_IS_WRITABLE"
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
 - IOCTL_DISK_IS_WRITABLE
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_IS_WRITABLE IOCTL


## -description


Determines whether the specified disk is writable.

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
  IOCTL_DISK_IS_WRITABLE,      // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSizeNULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>
 

 

