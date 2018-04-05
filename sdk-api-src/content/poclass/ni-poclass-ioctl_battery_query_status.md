---
UID: NI:poclass.IOCTL_BATTERY_QUERY_STATUS
title: IOCTL_BATTERY_QUERY_STATUS
author: windows-driver-content
description: Retrieves the current status of the battery.
old-location: base\ioctl_battery_query_status.htm
old-project: Power
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IOCTL_BATTERY_QUERY_STATUS, IOCTL_BATTERY_QUERY_STATUS control code, _win32_ioctl_battery_query_status, base.ioctl_battery_query_status, batclass/IOCTL_BATTERY_QUERY_STATUS, poclass/IOCTL_BATTERY_QUERY_STATUS
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
-	IOCTL_BATTERY_QUERY_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOCTL_BATTERY_QUERY_STATUS IOCTL


## -description


Retrieves the current status of the battery.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



This battery IOCTL retrieves the status of the battery at the time the operation returns. The input parameter 
    structure, <a href="https://msdn.microsoft.com/1750fe0f-ba3d-4118-938c-789c6d62c3f7">BATTERY_WAIT_STATUS</a>, indicates when 
    the battery status is to be processed and returned.

Requests for battery status can be for immediate return or can be set to wait for a particular condition 
    before completing. For example, a request for battery information can be made that waits until the battery 
    capacity reaches a specified point or the battery state changes.

All requests for battery information will complete with the status of 
    <b>ERROR_FILE_NOT_FOUND</b> whenever the <b>BatteryTag</b> element of 
    the request does not match that of the current battery tag. (See 
    <a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Tags</a> for more information.) This is used to 
    ensure that the returned battery information matches that of the requested battery.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/17e3c779-91ba-4901-9435-b73dedbf0b89">Enumerating Battery Devices</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a>



<a href="https://msdn.microsoft.com/1750fe0f-ba3d-4118-938c-789c6d62c3f7">BATTERY_WAIT_STATUS</a>



<a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Information</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/4cc89b89-ab33-47c2-8327-9627cbd1595e">IOCTL_BATTERY_QUERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a>



<a href="https://msdn.microsoft.com/b827983d-5fb8-43f2-b732-541d16b3eb7b">IOCTL_BATTERY_SET_INFORMATION</a>



<a href="https://msdn.microsoft.com/027fffdb-62a1-47d8-b69f-c2fcf7f9ac97">Power Management Control Codes</a>
 

 

