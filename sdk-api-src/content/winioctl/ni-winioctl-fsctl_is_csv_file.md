---
UID: NI:winioctl.FSCTL_IS_CSV_FILE
title: FSCTL_IS_CSV_FILE
author: windows-sdk-content
description: Determines whether a file is stored on a CSVFS volume, or retrieves namespace information.
old-location: fs\fsctl_is_csv_file.htm
tech.root: FileIO
ms.assetid: E2AB8999-7EF5-4F57-BCFB-79FBECE2E998
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_IS_CSV_FILE, FSCTL_IS_CSV_FILE control, FSCTL_IS_CSV_FILE control code [Files], fs.fsctl_is_csv_file, winioctl/FSCTL_IS_CSV_FILE
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_IS_CSV_FILE
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
- FSCTL_IS_CSV_FILE
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_IS_CSV_FILE IOCTL


## -description


Determines whether a file is stored on a CSVFS volume, or retrieves namespace information.

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
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 FSCTL_IS_CSV_FILE,             // dwIoControlCode
                 (LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
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




## -remarks



To determine whether a file is stored on a CSVFS volume, simply leave the <i>lpInBuffer</i> 
    parameter empty. If the file is on a CSVFS volume, the <i>lpOutBuffer</i> parameter will 
    contain <b>ERROR_SUCCESS</b>.

To retrieve namespace information, specify a pointer to the same 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_namespace_info">CSV_NAMESPACE_INFO</a> structure that is initially empty 
    (except for the <b>Version</b> member) in both the <i>lpInBuffer</i> and 
    <i>lpOutBuffer</i> parameters. The information in that structure is filled in by the function 
    call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_namespace_info">CSV_NAMESPACE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

