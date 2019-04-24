---
UID: NI:winioctl.FSCTL_IS_VOLUME_OWNED_BYCSVFS
title: FSCTL_IS_VOLUME_OWNED_BYCSVFS
author: windows-sdk-content
description: Determines whether a volume is locked by CSVFS.
old-location: fs\fsctl_is_volume_owned_bycsvfs.htm
tech.root: FileIO
ms.assetid: AA9D31DD-352C-4509-A5F3-55DC1C685E33
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_IS_VOLUME_OWNED_BYCSVFS, FSCTL_IS_VOLUME_OWNED_BYCSVFS control, FSCTL_IS_VOLUME_OWNED_BYCSVFS control code [Files], fs.fsctl_is_volume_owned_bycsvfs, winioctl/FSCTL_IS_VOLUME_OWNED_BYCSVFS
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
 - FSCTL_IS_VOLUME_OWNED_BYCSVFS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_IS_VOLUME_OWNED_BYCSVFS IOCTL


## -description


Determines whether a volume is locked by CSVFS.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_IS_VOLUME_OWNED_BYCSVFS, // dwIoControlCode
  NULL,                          // input buffer
  0,                             // size of input buffer
  (LPVOID) lpOutBuffer,          // lpOutBuffer
  (DWORD) nOutBufferSize,        // nOutBufferSize
  (LPDWORD) lpBytesReturned,     // number of bytes returned
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



If the volume is locked on behalf of CSVFS, the control code returns information that is sent to an NTFS 
    volume. If the volume is locked (using <a href="https://msdn.microsoft.com/b59b5c5e-6719-47a8-8810-14b60204e5ed">FSCTL_LOCK_VOLUME</a>) 
    from a request that originates from CSVFS, then the 
    <a href="https://msdn.microsoft.com/F189E0F9-F711-4AB6-8237-775855FCD290">CSV_IS_OWNED_BY_CSVFS</a> structure's 
    <b>OwnedByCSVFS</b> member has a value of <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/F189E0F9-F711-4AB6-8237-775855FCD290">CSV_IS_OWNED_BY_CSVFS</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

