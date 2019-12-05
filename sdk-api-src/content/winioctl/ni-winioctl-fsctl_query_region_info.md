---
UID: NI:winioctl.FSCTL_QUERY_REGION_INFO
title: FSCTL_QUERY_REGION_INFO
description: Retrieves the storage tier regions defined for a volume that supports data tiering.
old-location: fs\fsctl_query_region_info.htm
tech.root: FileIO
ms.assetid: 292D377B-F7DE-489B-B686-0CE5278360BC
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_REGION_INFO, FSCTL_QUERY_REGION_INFO control, FSCTL_QUERY_REGION_INFO control code [Files], fs.fsctl_query_region_info, winioctl/FSCTL_QUERY_REGION_INFO
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_QUERY_REGION_INFO
dev_langs:
- c++
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
- WinIoctl.h
api_name:
- FSCTL_QUERY_REGION_INFO
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_REGION_INFO IOCTL


## -description


Retrieves the storage tier regions defined for a volume that supports data tiering.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        FSCTL_QUERY_REGION_INFO, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
                    (DWORD)        nOutBufferSize,  // size of output buffer
                    (LPDWORD)      lpBytesReturned, // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

