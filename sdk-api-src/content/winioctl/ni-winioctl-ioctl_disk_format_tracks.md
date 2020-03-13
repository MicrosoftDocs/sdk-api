---
UID: NI:winioctl.IOCTL_DISK_FORMAT_TRACKS
title: IOCTL_DISK_FORMAT_TRACKS
description: Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use IOCTL_DISK_FORMAT_TRACKS_EXinstead.
old-location: fs\ioctl_disk_format_tracks.htm
tech.root: FileIO
ms.assetid: 9d6e0865-4b4d-4334-855b-3fbd26832591
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_FORMAT_TRACKS, IOCTL_DISK_FORMAT_TRACKS control, IOCTL_DISK_FORMAT_TRACKS control code [Files], _win32_ioctl_disk_format_tracks, base.ioctl_disk_format_tracks, fs.ioctl_disk_format_tracks, winioctl/IOCTL_DISK_FORMAT_TRACKS
f1_keywords:
- winioctl/IOCTL_DISK_FORMAT_TRACKS
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
- IOCTL_DISK_FORMAT_TRACKS
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_FORMAT_TRACKS IOCTL


## -description


Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks_ex">IOCTL_DISK_FORMAT_TRACKS_EX</a>instead.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_FORMAT_TRACKS,    // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-format_parameters">FORMAT_PARAMETERS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks_ex">IOCTL_DISK_FORMAT_TRACKS_EX</a>
 

 

