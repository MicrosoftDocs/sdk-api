---
UID: NI:winioctl.FSCTL_USN_TRACK_MODIFIED_RANGES
title: FSCTL_USN_TRACK_MODIFIED_RANGES

description: Enables range tracking feature for update sequence number (USN) change journal stream on a target volume, or modifies already enabled range tracking parameters.
old-location: fs\fsctl_usn_track_modified_ranges.htm
tech.root: FileIO
ms.assetid: 258E16B2-B6E8-44BB-8073-B1BEDD4FA86A

ms.date: 12/05/2018
ms.keywords: FSCTL_USN_TRACK_MODIFIED_RANGES, FSCTL_USN_TRACK_MODIFIED_RANGES control, FSCTL_USN_TRACK_MODIFIED_RANGES control code [Files], fs.fsctl_usn_track_modified_ranges, winioctl/FSCTL_USN_TRACK_MODIFIED_RANGES
ms.topic: ioctl
f1_keywords: 
 - "winioctl/FSCTL_USN_TRACK_MODIFIED_RANGES"
dev_langs:
 - c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - FSCTL_USN_TRACK_MODIFIED_RANGES
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_USN_TRACK_MODIFIED_RANGES IOCTL


## -description


Enables range tracking feature for update sequence number (USN) change journal stream on a target volume, or modifies already enabled range tracking parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to volume
                    (DWORD)        FSCTL_USN_TRACK_MODIFIED_RANGES, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // lpOutbuffer
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




## -remarks



For the implications of overlapped I/O on this operation, see the Remarks section of the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

You can use <b>FSCTL_USN_TRACK_MODIFIED_RANGES</b> to enable range tracking for the first time for a volume. After the enabling range tracking, the state and parameters will be persisted for that volume and on next reboot the range tracking will be initialized read from the persisted parameters.

You can also use <b>FSCTL_USN_TRACK_MODIFIED_RANGES</b> to modify an existing change journal stream range track parameter. If range tracking is already exists, <b>FSCTL_USN_TRACK_MODIFIED_RANGES</b> sets it to the parameters provided in the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-usn_track_modified_ranges">USN_TRACK_MODIFIED_RANGES</a> structure. The chunk size or file size threshold can only be lowered from previous values. Once enabled, range tracking feature cannot be disabled unless the journal is deleted. 

To retrieve a handle to a volume, call <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the <i>lpFileName</i> parameter set to a string in the following form:

\\.\X:

In the preceding string, X is the letter identifying the drive on which the volume appears. The volume must be NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:

<b>fsutil fsinfo ntfsinfo </b><i>X</i><b>:</b>

where <i>X</i> is the drive letter of the volume.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>
 

 

