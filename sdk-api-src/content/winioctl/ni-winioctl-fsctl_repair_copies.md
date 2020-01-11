---
UID: NI:winioctl.FSCTL_REPAIR_COPIES
title: FSCTL_REPAIR_COPIES
description: Repair data corruption by selecting the proper copy to use.
old-location: fs\fsctl_repair_copies.htm
tech.root: FileIO
ms.assetid: 1970ed09-5f37-4cc9-98c5-982629676fe4
ms.date: 12/05/2018
ms.keywords: FSCTL_REPAIR_COPIES, FSCTL_REPAIR_COPIES control, FSCTL_REPAIR_COPIES control code [Files], fs.fsctl_repair_copies, winioctl/FSCTL_REPAIR_COPIES
f1_keywords:
- winioctl/FSCTL_REPAIR_COPIES
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_REPAIR_COPIES IOCTL


## -description


Repair data corruption by selecting the proper copy to use. This control code was 
    introduced in Windows 8 and Windows Server 2012 for use on  on Storage Spaces and Streams on 
    NTFS and ReFS and non-integrity streams on ReFS (streams with integrity on ReFS handle this automatically.)

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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_integrity_information">FSCTL_GET_INTEGRITY_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-repair_copies_output">REPAIR_COPIES_OUTPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

