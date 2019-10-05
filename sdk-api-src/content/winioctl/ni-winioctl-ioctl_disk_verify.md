---
UID: NI:winioctl.IOCTL_DISK_VERIFY
title: IOCTL_DISK_VERIFY
author: windows-sdk-content
description: Verifies the specified extent on a fixed disk.
old-location: fs\ioctl_disk_verify.htm
tech.root: FileIO
ms.assetid: 156b217d-6cdc-4802-b711-8845934e277b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_VERIFY, IOCTL_DISK_VERIFY control, IOCTL_DISK_VERIFY control code [Files], _win32_ioctl_disk_verify, base.ioctl_disk_verify, fs.ioctl_disk_verify, winioctl/IOCTL_DISK_VERIFY
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_DISK_VERIFY
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
- IOCTL_DISK_VERIFY
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_VERIFY IOCTL


## -description


Verifies the specified extent on a fixed disk.

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
  IOCTL_DISK_VERIFY,           // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  NULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-verify_information">VERIFY_INFORMATION</a>
 

 

