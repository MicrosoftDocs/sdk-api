---
UID: NI:winioctl.IOCTL_STORAGE_PROTOCOL_COMMAND
title: IOCTL_STORAGE_PROTOCOL_COMMAND
description: Windows applications can use this control code to return properties of a storage device or adapter. The request indicates the kind of information to retrieve, such as inquiry data for a device or capabilities and limitations of an adapter.
old-location: fs\ioctl_storage_protocol_command.htm
tech.root: FileIO
ms.assetid: 77027740-CDFD-422A-B458-C36B2E346EFD
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_PROTOCOL_COMMAND, IOCTL_STORAGE_PROTOCOL_COMMAND control, IOCTL_STORAGE_PROTOCOL_COMMAND control code [Files], fs.ioctl_storage_protocol_command, winioctl/IOCTL_STORAGE_PROTOCOL_COMMAND
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_STORAGE_QUERY_PROPERTY
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
- winioctl.h
api_name:
- IOCTL_STORAGE_QUERY_PROPERTY
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_PROTOCOL_COMMAND IOCTL


## -description

Windows applications can use <b>IOCTL_STORAGE_PROTOCOL_COMMAND</b> to conduct pass-through of protocol specific commands to the storage device or adapter. The request indicates the bus specific command which is further sent to a specific type of device to process. For more information, see the page on <a href="https://docs.microsoft.com/en-us/windows/win32/fileio/working-with-nvme-devices#using-ioctl_storage_protocol_command-to-send-commands">working with NVMe drives</a>.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_STORAGE_PROTOCOL_COMMAND, // dwIoControlCode
                    (LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
                    (DWORD)        nOutBufferSize,  // size of output buffer
                    (LPDWORD)      lpBytesReturned, // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
</pre>
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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-storage_property_query">STORAGE_PROPERTY_QUERY</a>
 

 

