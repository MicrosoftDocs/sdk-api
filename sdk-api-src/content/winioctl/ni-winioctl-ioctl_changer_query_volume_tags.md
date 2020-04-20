---
UID: NI:winioctl.IOCTL_CHANGER_QUERY_VOLUME_TAGS
title: IOCTL_CHANGER_QUERY_VOLUME_TAGS
description: Retrieves the volume tag information for the specified elements.helpviewer_keywords: ["IOCTL_CHANGER_QUERY_VOLUME_TAGS","IOCTL_CHANGER_QUERY_VOLUME_TAGS control","IOCTL_CHANGER_QUERY_VOLUME_TAGS control code","_win32_ioctl_changer_query_volume_tags","base.ioctl_changer_query_volume_tags","winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS"]
old-location: base\ioctl_changer_query_volume_tags.htm
tech.root: devio
ms.assetid: 67c440e1-cef8-459d-b811-0b483ff51e7e
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_QUERY_VOLUME_TAGS, IOCTL_CHANGER_QUERY_VOLUME_TAGS control, IOCTL_CHANGER_QUERY_VOLUME_TAGS control code, _win32_ioctl_changer_query_volume_tags, base.ioctl_changer_query_volume_tags, winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS
f1_keywords:
- winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
- IOCTL_CHANGER_QUERY_VOLUME_TAGS
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_QUERY_VOLUME_TAGS IOCTL


## -description


Retrieves the volume tag information for the specified elements.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_CHANGER_QUERY_VOLUME_TAGS, // dwIoControlCode(LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
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




<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-changer_send_volume_tag_information">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-read_element_address_info">READ_ELEMENT_ADDRESS_INFO</a>
 

 

