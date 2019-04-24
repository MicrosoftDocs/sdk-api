---
UID: NI:winioctl.FSCTL_REPAIR_COPIES
title: FSCTL_REPAIR_COPIES
author: windows-sdk-content
description: Repair data corruption by selecting the proper copy to use.
old-location: fs\fsctl_repair_copies.htm
tech.root: FileIO
ms.assetid: 1970ed09-5f37-4cc9-98c5-982629676fe4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_REPAIR_COPIES, FSCTL_REPAIR_COPIES control, FSCTL_REPAIR_COPIES control code [Files], fs.fsctl_repair_copies, winioctl/FSCTL_REPAIR_COPIES
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FSCTL_REPAIR_COPIES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_REPAIR_COPIES IOCTL


## -description


Repair data corruption by selecting the proper copy to use. This control code was 
    introduced in Windows 8 and Windows Server 2012 for use on  on Storage Spaces and Streams on 
    NTFS and ReFS and non-integrity streams on ReFS (streams with integrity on ReFS handle this automatically.)

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)  hDevice,             // handle to file or directory
                 (DWORD)   FSCTL_REPAIR_COPIES, // dwIoControlCode
                 (LPDWORD) pInBuffer,           // REPAIR_COPIES_INPUT
                 (DWORD)   InBufferSize,        // size of input buffer
                 (LPDWORD) pOutBuffer,          // REPAIR_COPIES_OUTPUT
                 (DWORD)   OutBufferSize,       // size of output buffer
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/5e003b2f-d38a-45f1-9b50-40af4087b0ce">FSCTL_GET_INTEGRITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3da7779-92e7-40bf-a889-dd2013e942ab">REPAIR_COPIES_OUTPUT</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

