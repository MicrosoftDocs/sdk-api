---
UID: NI:winioctl.IOCTL_CHANGER_GET_ELEMENT_STATUS
title: IOCTL_CHANGER_GET_ELEMENT_STATUS
description: Retrieves the status of all elements or a specified number of elements of a particular type.
old-location: base\ioctl_changer_get_element_status.htm
tech.root: devio
ms.assetid: b5266a22-1f7b-423d-b3c1-7e455d87dd2b
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_GET_ELEMENT_STATUS, IOCTL_CHANGER_GET_ELEMENT_STATUS control, IOCTL_CHANGER_GET_ELEMENT_STATUS control code, _win32_ioctl_changer_get_element_status, base.ioctl_changer_get_element_status, winioctl/IOCTL_CHANGER_GET_ELEMENT_STATUS
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_CHANGER_GET_ELEMENT_STATUS
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
- IOCTL_CHANGER_GET_ELEMENT_STATUS
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_GET_ELEMENT_STATUS IOCTL


## -description


Retrieves the status of all elements or a specified number of elements of a particular type.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_CHANGER_GET_ELEMENT_STATUS, // dwIoControlCode(LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
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




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_element_status">CHANGER_ELEMENT_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_element_status_ex">CHANGER_ELEMENT_STATUS_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_read_element_status">CHANGER_READ_ELEMENT_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

