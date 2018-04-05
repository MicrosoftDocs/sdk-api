---
UID: NI:poclass.IOCTL_BATTERY_QUERY_TAG
title: IOCTL_BATTERY_QUERY_TAG
author: windows-driver-content
description: Retrieves the battery's current tag.
old-location: base\ioctl_battery_query_tag.htm
old-project: Power
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCTL_BATTERY_QUERY_TAG, IOCTL_BATTERY_QUERY_TAG control code, _win32_ioctl_battery_query_tag, base.ioctl_battery_query_tag, batclass/IOCTL_BATTERY_QUERY_TAG, poclass/IOCTL_BATTERY_QUERY_TAG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: poclass.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	BatClass.h
api_name:
-	IOCTL_BATTERY_QUERY_TAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_BATTERY_QUERY_TAG IOCTL


## -description


Retrieves the battery's current tag.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure</pre>
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



This battery IOCTL retrieves the battery's current tag. The battery tag is a unique nonzero value that changes 
    when the physical battery is reinserted, replaced, or undergoes any characteristic changes. See the 
    Battery Tags section in the 
    <a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Information</a> overview topic for more detail on 
    when a battery tag changes, how to detect the change, and how an application should proceed after a battery tag 
    change. When a battery is not present, this request will wait the indicated time, and if there is still no battery 
    present, then it will return <b>ERROR_FILE_NOT_FOUND</b> and set the battery tag to 
    <b>BATTERY_TAG_INVALID</b>. (See 
    Battery Information for more information.)

All requests for other battery information require the caller to supply the matching battery tag. This ensures 
    that the caller is receiving information for the same battery for every request and ensures that the caller is 
    aware of battery changes without constant polling.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/17e3c779-91ba-4901-9435-b73dedbf0b89">Enumerating Battery Devices</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Information</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a>



<a href="https://msdn.microsoft.com/b827983d-5fb8-43f2-b732-541d16b3eb7b">IOCTL_BATTERY_SET_INFORMATION</a>



<a href="https://msdn.microsoft.com/027fffdb-62a1-47d8-b69f-c2fcf7f9ac97">Power Management Control Codes</a>
 

 

