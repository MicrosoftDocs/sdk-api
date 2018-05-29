---
UID: NI:winioctl.IOCTL_CHANGER_GET_ELEMENT_STATUS
title: IOCTL_CHANGER_GET_ELEMENT_STATUS
author: windows-sdk-content
description: Retrieves the status of all elements or a specified number of elements of a particular type.
old-location: base\ioctl_changer_get_element_status.htm
old-project: DevIO
ms.assetid: b5266a22-1f7b-423d-b3c1-7e455d87dd2b
ms.author: windowssdkdev
ms.date: 04/03/2018
ms.keywords: IOCTL_CHANGER_GET_ELEMENT_STATUS, IOCTL_CHANGER_GET_ELEMENT_STATUS control, IOCTL_CHANGER_GET_ELEMENT_STATUS control code, _win32_ioctl_changer_get_element_status, base.ioctl_changer_get_element_status, winioctl/IOCTL_CHANGER_GET_ELEMENT_STATUS
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
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	IOCTL_CHANGER_GET_ELEMENT_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_CHANGER_GET_ELEMENT_STATUS IOCTL


## -description


Retrieves the status of all elements or a specified number of elements of a particular type.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_CHANGER_GET_ELEMENT_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551461">CHANGER_ELEMENT_STATUS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551462">CHANGER_ELEMENT_STATUS_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551477">CHANGER_READ_ELEMENT_STATUS</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

