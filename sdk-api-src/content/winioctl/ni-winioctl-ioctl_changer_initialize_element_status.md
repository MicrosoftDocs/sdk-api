---
UID: NI:winioctl.IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
title: IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
author: windows-sdk-content
description: Initializes the status of all elements or the specified elements of a particular type.
old-location: base\ioctl_changer_initialize_element_status.htm
tech.root: devio
ms.assetid: be054a22-cde4-4efd-bd66-eb67b007fd19
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS, IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control, IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control code, _win32_ioctl_changer_initialize_element_status, base.ioctl_changer_initialize_element_status, winioctl/IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS IOCTL


## -description


Initializes the status of all elements or the specified elements of a particular type.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                        // handle to device
  IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS, // dwIoControlCode(LPVOID) lpInBuffer,                     // input buffer
  (DWORD) nInBufferSize,                   // size of input buffer
  NULL,                                    // lpOutBuffer0,                                       // nOutBufferSize(LPDWORD) lpBytesReturned,               // number of bytes returned
  (LPOVERLAPPED) lpOverlapped              // OVERLAPPED structure
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




<a href="https://msdn.microsoft.com/593df7e3-dd2b-4ba9-b7a0-ed6ea06586ba">CHANGER_INITIALIZE_ELEMENT_STATUS</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

