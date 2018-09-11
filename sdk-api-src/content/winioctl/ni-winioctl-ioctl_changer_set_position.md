---
UID: NI:winioctl.IOCTL_CHANGER_SET_POSITION
title: IOCTL_CHANGER_SET_POSITION
author: windows-sdk-content
description: Sets the changer's robotic transport mechanism to the specified element address. This optimizes moving or exchanging media by positioning the transport beforehand.
old-location: base\ioctl_changer_set_position.htm
tech.root: devio
ms.assetid: 1c3348d5-6d22-40cb-bf4f-e843819884b9
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IOCTL_CHANGER_SET_POSITION, IOCTL_CHANGER_SET_POSITION control, IOCTL_CHANGER_SET_POSITION control code, _win32_ioctl_changer_set_position, base.ioctl_changer_set_position, winioctl/IOCTL_CHANGER_SET_POSITION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - IOCTL_CHANGER_SET_POSITION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_SET_POSITION IOCTL


## -description


Sets the changer's robotic transport mechanism to the specified element address. This optimizes moving or exchanging media by positioning the transport beforehand.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_CHANGER_SET_POSITION,   // dwIoControlCode(LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer0,                            // nOutBufferSize(LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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




<a href="https://msdn.microsoft.com/7bffff12-666d-4203-bddd-32f279d18fb4">CHANGER_SET_POSITION</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

