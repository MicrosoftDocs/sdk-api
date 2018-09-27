---
UID: NI:winioctl.IOCTL_DISK_SET_DRIVE_LAYOUT_EX
title: IOCTL_DISK_SET_DRIVE_LAYOUT_EX
author: windows-sdk-content
description: Partitions a disk according to the specified drive layout and partition information data.
old-location: fs\ioctl_disk_set_drive_layout_ex.htm
tech.root: fileio
ms.assetid: a600e841-c692-4aa4-bea2-a33931d9b007
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOCTL_DISK_SET_DRIVE_LAYOUT_EX, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control code [Files], _win32_ioctl_disk_set_drive_layout_ex, base.ioctl_disk_set_drive_layout_ex, fs.ioctl_disk_set_drive_layout_ex, winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_SET_DRIVE_LAYOUT_EX IOCTL


## -description


Partitions a disk according to the specified drive layout and partition information data.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,               // handle to device
  IOCTL_DISK_SET_DRIVE_LAYOUT_EX, // dwIoControlCode(LPVOID) lpInBuffer,            // input buffer
  (DWORD) nInBufferSize,          // size of the input buffer
  NULL,                           // lpOutBuffer0,                              // nOutBufferSize 
  (LPDWORD) lpBytesReturned,      // number of bytes returned
  (LPOVERLAPPED) lpOverlapped     // OVERLAPPED structure
);
```



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



When specifying a <b>GUID</b> partition table (GPT) as the <a href="https://msdn.microsoft.com/254e4ea1-d0c8-4033-b8af-e5dbfb7c7da8">PARTITION_STYLE</a> of the <a href="https://msdn.microsoft.com/ec4a1ef9-ff2e-41b3-951b-241c545f256b">CREATE_DISK</a> structure, an application should wait for the MSR partition arrival before sending the <b>IOCTL_DISK_SET_DRIVE_LAYOUT_EX</b> control code. For more information about device notification, see <a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>.

When creating and manipulating an Extended Boot Record (EBR), the first entry of the EBR should point to the logical drive that immediately follows the EBR and the next EBR should lie after the end of the current logical drive and before the start of the next logical drive. For more information, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=145245">Disk Concepts and Troubleshooting</a>.

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/8cace6a5-666a-4d35-a557-6bf0564dbe58">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://msdn.microsoft.com/381c87a8-fe40-4251-a4df-dddc9e2a126d">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/21507182-5a33-4e58-b5ed-3724feefa4ed">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>
 

 

