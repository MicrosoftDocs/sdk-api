---
UID: NI:winioctl.FSCTL_CSV_CONTROL
title: FSCTL_CSV_CONTROL

description: Retrieves the results of a CSV control operation.
old-location: fs\fsctl_csv_control.htm
tech.root: FileIO
ms.assetid: 6CCCD5CA-FF29-41D4-B687-E403CADABF84

ms.date: 12/05/2018
ms.keywords: FSCTL_CSV_CONTROL, FSCTL_CSV_CONTROL control, FSCTL_CSV_CONTROL control code [Files], fs.fsctl_csv_control, winioctl/FSCTL_CSV_CONTROL
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_CSV_CONTROL
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
- FSCTL_CSV_CONTROL
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_CSV_CONTROL IOCTL


## -description


Retrieves the results of a CSV control operation.

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
                 FSCTL_CSV_CONTROL,             // dwIoControlCode
                 (LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 (LPVOID) lpOutBuffer,          // output buffer
                 (DWORD) nOutBufferSize,        // size of output buffer
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




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-csv_control_op">CSV_CONTROL_OP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_control_param">CSV_CONTROL_PARAM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_file_revision">CSV_QUERY_FILE_REVISION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_mds_path">CSV_QUERY_MDS_PATH</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-csv_query_redirect_state">CSV_QUERY_REDIRECT_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

