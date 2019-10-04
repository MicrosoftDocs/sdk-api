---
UID: NI:winioctl.IOCTL_STORAGE_EJECTION_CONTROL
title: IOCTL_STORAGE_EJECTION_CONTROL
author: windows-sdk-content
description: Enables or disables the mechanism that ejects media. Disabling the mechanism locks the drive.
old-location: base\ioctl_storage_ejection_control.htm
tech.root: devio
ms.assetid: d31aae7b-df93-419d-9a53-80a601a3c437
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_EJECTION_CONTROL, IOCTL_STORAGE_EJECTION_CONTROL control, IOCTL_STORAGE_EJECTION_CONTROL control code, _win32_ioctl_storage_ejection_control, base.ioctl_storage_ejection_control, winioctl/IOCTL_STORAGE_EJECTION_CONTROL
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_STORAGE_EJECTION_CONTROL
dev_langs:
 - c++
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
- IOCTL_STORAGE_EJECTION_CONTROL
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_EJECTION_CONTROL IOCTL


## -description


Enables or disables the mechanism that ejects media. Disabling the mechanism locks the drive.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_STORAGE_EJECTION_CONTROL,  // dwIoControlCode(LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  NULL,                            // lpOutBuffer0,                               // nOutBufferSize(LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
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



The driver tracks 
<b>IOCTL_STORAGE_EJECTION_CONTROL</b> requests by caller. It ignores requests to enable the ejection mechanism unless it has received a request to disable the ejection mechanism from the same caller. This prevents other callers from unlocking the drive.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-prevent_media_removal">PREVENT_MEDIA_REMOVAL</a>
 

 

