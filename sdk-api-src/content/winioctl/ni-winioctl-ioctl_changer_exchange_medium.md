---
UID: NI:winioctl.IOCTL_CHANGER_EXCHANGE_MEDIUM
title: IOCTL_CHANGER_EXCHANGE_MEDIUM
author: windows-sdk-content
description: Moves a piece of media from a source element to one destination, and the piece of media originally in the first destination to a second destination.
old-location: base\ioctl_changer_exchange_medium.htm
old-project: devio
ms.assetid: 40550df0-9da4-4b02-bd57-23eae78c68df
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IOCTL_CHANGER_EXCHANGE_MEDIUM, IOCTL_CHANGER_EXCHANGE_MEDIUM control, IOCTL_CHANGER_EXCHANGE_MEDIUM control code, _win32_ioctl_changer_exchange_medium, base.ioctl_changer_exchange_medium, winioctl/IOCTL_CHANGER_EXCHANGE_MEDIUM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_CHANGER_EXCHANGE_MEDIUM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_CHANGER_EXCHANGE_MEDIUM IOCTL


## -description


Moves a piece of media from a source element to one destination, and the piece of media originally in the first destination to a second destination.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  IOCTL_CHANGER_EXCHANGE_MEDIUM, // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
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



To swap two pieces of media, specify the source as the value for the second destination.




## -see-also




<a href="https://msdn.microsoft.com/a35c9da8-7632-4aa1-a1a7-030ffce727b7">CHANGER_EXCHANGE_MEDIUM</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

