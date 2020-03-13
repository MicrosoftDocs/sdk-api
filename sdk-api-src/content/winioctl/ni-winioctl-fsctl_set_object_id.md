---
UID: NI:winioctl.FSCTL_SET_OBJECT_ID
title: FSCTL_SET_OBJECT_ID
description: Sets the object identifier for the specified file or directory.
old-location: fs\fsctl_set_object_id.htm
tech.root: FileIO
ms.assetid: eb131a33-96c8-40fc-92be-05522676541a
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_OBJECT_ID, FSCTL_SET_OBJECT_ID control, FSCTL_SET_OBJECT_ID control code [Files], _win32_fsctl_set_object_id, base.fsctl_set_object_id, fs.fsctl_set_object_id, winioctl/FSCTL_SET_OBJECT_ID
f1_keywords:
- winioctl/FSCTL_SET_OBJECT_ID
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- FSCTL_SET_OBJECT_ID
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_OBJECT_ID IOCTL


## -description


Sets the object identifier for the specified file or directory.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to device
  FSCTL_SET_OBJECT_ID,        // dwIoControlCode(LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  NULL,                       // lpOutBuffer0,                          // nOutBufferSize(LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



Object identifiers are used  to track files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data. 

Use this operation to explicitly set an object identifier to a value you provide. Attempting to set an object identifier on an object that already has an object identifier will fail. An attempt to use an object identifier that is already in use on the volume will also fail. Use the 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id">FSCTL_CREATE_OR_GET_OBJECT_ID</a> operation to have the NTFS file system generate an object identifier if the object does not already have one.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_objectid_buffer">FILE_OBJECTID_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id">FSCTL_CREATE_OR_GET_OBJECT_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_delete_object_id">FSCTL_DELETE_OBJECT_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_object_id">FSCTL_GET_OBJECT_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_set_object_id_extended">FSCTL_SET_OBJECT_ID_EXTENDED</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers">Object Identifiers</a>
 

 

