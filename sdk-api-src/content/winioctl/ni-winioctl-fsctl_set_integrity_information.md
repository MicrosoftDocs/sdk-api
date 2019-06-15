---
UID: NI:winioctl.FSCTL_SET_INTEGRITY_INFORMATION
title: FSCTL_SET_INTEGRITY_INFORMATION
author: windows-sdk-content
description: Retrieves the integrity status of a file or directory on a ReFS volume.
old-location: fs\fsctl_set_integrity_information.htm
tech.root: FileIO
ms.assetid: bd5be96d-6fdc-4fad-9d01-81b913a5b653
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_INTEGRITY_INFORMATION, FSCTL_SET_INTEGRITY_INFORMATION control, FSCTL_SET_INTEGRITY_INFORMATION control code [Files], fs.fsctl_set_integrity_information, winioctl/FSCTL_SET_INTEGRITY_INFORMATION
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
 - FSCTL_SET_INTEGRITY_INFORMATION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_INTEGRITY_INFORMATION IOCTL


## -description


Retrieves the integrity status of a file or directory on a ReFS volume.

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
DeviceIoControl( (HANDLE) hDevice,                // handle to file or directory
                 FSCTL_SET_INTEGRITY_INFORMATION, // dwIoControlCode
                 (LPDWORD) pInBuffer,             // FSCTL_SET_INTEGRITY_INFORMATION_BUFFER 
                 (DWORD) InBufferSize,            // size of input buffer
                 (LPDWORD) NULL,                  // pOutBuffer
                 (DWORD) 0,                       // OutBufferSize
                 (LPDWORD) NULL,                  // lpBytesReturned
                 (LPOVERLAPPED) lpOverlapped );   // OVERLAPPED structure</pre>
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



The integrity status can only be changed for empty files.

If the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-replacefilea">ReplaceFile</a> is used to replace a file with 
    integrity set, and the <i>lpBackupFileName</i> parameter points to a location that does not 
    have integrity set, the integrity status of the original file will not be persisted.

Writes to integrity streams are always cluster-sized. Reads from integrity streams are always done in  16 KB 
    blocks. This can lead to reads failing even when the corrupt area is outside the region being read. For example, 
    if 4 KB is read at offset 0 in a file and there is corruption starting 12 KB into the file, a read would fail with 
    <b>ERROR_DATA_CHECKSUM_ERROR</b> (0x143).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_integrity_information">FSCTL_GET_INTEGRITY_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_fsctl_set_integrity_information_buffer">FSCTL_SET_INTEGRITY_INFORMATION_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

