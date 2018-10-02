---
UID: NI:winioctl.IOCTL_DISK_FORMAT_TRACKS
title: IOCTL_DISK_FORMAT_TRACKS
author: windows-sdk-content
description: Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use IOCTL_DISK_FORMAT_TRACKS_EXinstead.
old-location: fs\ioctl_disk_format_tracks.htm
tech.root: fileio
ms.assetid: 9d6e0865-4b4d-4334-855b-3fbd26832591
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IOCTL_DISK_FORMAT_TRACKS, IOCTL_DISK_FORMAT_TRACKS control, IOCTL_DISK_FORMAT_TRACKS control code [Files], _win32_ioctl_disk_format_tracks, base.ioctl_disk_format_tracks, fs.ioctl_disk_format_tracks, winioctl/IOCTL_DISK_FORMAT_TRACKS
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
 - IOCTL_DISK_FORMAT_TRACKS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_FORMAT_TRACKS IOCTL


## -description


Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use <a href="https://msdn.microsoft.com/50ca069e-efc5-46d8-bf8f-ff44e1593a76">IOCTL_DISK_FORMAT_TRACKS_EX</a>instead.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_FORMAT_TRACKS,    // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/81fcfd8e-abb9-4c0b-b23d-302aa3645a6f">FORMAT_PARAMETERS</a>



<a href="https://msdn.microsoft.com/50ca069e-efc5-46d8-bf8f-ff44e1593a76">IOCTL_DISK_FORMAT_TRACKS_EX</a>
 

 

