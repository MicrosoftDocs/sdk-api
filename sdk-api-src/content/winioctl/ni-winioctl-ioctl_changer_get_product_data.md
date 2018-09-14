---
UID: NI:winioctl.IOCTL_CHANGER_GET_PRODUCT_DATA
title: IOCTL_CHANGER_GET_PRODUCT_DATA
author: windows-sdk-content
description: Retrieves the product data for the specified device.
old-location: base\ioctl_changer_get_product_data.htm
tech.root: devio
ms.assetid: 60744666-fb37-4263-8f4a-e7e043e6b71e
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IOCTL_CHANGER_GET_PRODUCT_DATA, IOCTL_CHANGER_GET_PRODUCT_DATA control, IOCTL_CHANGER_GET_PRODUCT_DATA control code, _win32_ioctl_changer_get_product_data, base.ioctl_changer_get_product_data, winioctl/IOCTL_CHANGER_GET_PRODUCT_DATA
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
 - IOCTL_CHANGER_GET_PRODUCT_DATA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_GET_PRODUCT_DATA IOCTL


## -description


Retrieves the product data for the specified device.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,               // handle to device
  IOCTL_CHANGER_GET_PRODUCT_DATA, // dwIoControlCodeNULL,                           // lpInBuffer0,                              // nInBufferSize(LPVOID) lpOutBuffer,           // output buffer
  (DWORD) nOutBufferSize,         // size of output buffer
  (LPDWORD) lpBytesReturned,      // number of bytes returned
  (LPOVERLAPPED) lpOverlapped     // OVERLAPPED structure
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




<a href="https://msdn.microsoft.com/b6756994-2c6f-4797-8fad-823d63632372">CHANGER_PRODUCT_DATA</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

