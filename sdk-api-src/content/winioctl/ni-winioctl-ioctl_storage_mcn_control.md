---
UID: NI:winioctl.IOCTL_STORAGE_MCN_CONTROL
title: IOCTL_STORAGE_MCN_CONTROL
description: Enables or disables media change notification. Disabling media change notification prevents the GUID_IO_MEDIA_ARRIVAL and GUID_IO_MEDIA_REMOVAL events.
old-location: base\ioctl_storage_mcn_control.htm
tech.root: devio
ms.assetid: 1122f27f-c1a6-49a9-b09a-5b33c451e1cc
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_MCN_CONTROL, IOCTL_STORAGE_MCN_CONTROL control, IOCTL_STORAGE_MCN_CONTROL control code, _win32_ioctl_storage_mcn_control, base.ioctl_storage_mcn_control, winioctl/IOCTL_STORAGE_MCN_CONTROL
f1_keywords:
- winioctl/IOCTL_STORAGE_MCN_CONTROL
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
- IOCTL_STORAGE_MCN_CONTROL
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_MCN_CONTROL IOCTL


## -description


Enables or disables media change notification. Disabling media change notification prevents the <b>GUID_IO_MEDIA_ARRIVAL</b> and <b>GUID_IO_MEDIA_REMOVAL</b> events.

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
  IOCTL_STORAGE_MCN_CONTROL,   // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

