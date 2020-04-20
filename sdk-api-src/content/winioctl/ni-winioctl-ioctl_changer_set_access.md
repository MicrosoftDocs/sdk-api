---
UID: NI:winioctl.IOCTL_CHANGER_SET_ACCESS
title: IOCTL_CHANGER_SET_ACCESS
description: Sets the state of the device's insert/eject port, door, or keypad.helpviewer_keywords: ["IOCTL_CHANGER_SET_ACCESS","IOCTL_CHANGER_SET_ACCESS control","IOCTL_CHANGER_SET_ACCESS control code","_win32_ioctl_changer_set_access","base.ioctl_changer_set_access","winioctl/IOCTL_CHANGER_SET_ACCESS"]
old-location: base\ioctl_changer_set_access.htm
tech.root: devio
ms.assetid: 567817d5-60cd-494c-94d9-0899e1142242
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_SET_ACCESS, IOCTL_CHANGER_SET_ACCESS control, IOCTL_CHANGER_SET_ACCESS control code, _win32_ioctl_changer_set_access, base.ioctl_changer_set_access, winioctl/IOCTL_CHANGER_SET_ACCESS
f1_keywords:
- winioctl/IOCTL_CHANGER_SET_ACCESS
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
- IOCTL_CHANGER_SET_ACCESS
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_SET_ACCESS IOCTL


## -description


Sets the state of the device's insert/eject port, door, or keypad.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_CHANGER_SET_ACCESS,     // dwIoControlCode(LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer0,                            // nOutBufferSize(LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_set_access">CHANGER_SET_ACCESS</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

