---
UID: NF:faxdev.FaxDevVirtualDeviceCreation
title: FaxDevVirtualDeviceCreation function
author: windows-sdk-content
description: The fax service calls the FaxDevVirtualDeviceCreation function during initialization to allow the fax service provider (FSP) to present virtual fax devices.
old-location: fax\_mfax_faxdevvirtualdevicecreation.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_48by.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: FaxDevVirtualDeviceCreation, FaxDevVirtualDeviceCreation function [Fax Service], _mfax_faxdevvirtualdevicecreation, fax._mfax_faxdevvirtualdevicecreation, faxdev/FaxDevVirtualDeviceCreation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevVirtualDeviceCreation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevVirtualDeviceCreation function


## -description


The fax service calls the <b>FaxDevVirtualDeviceCreation</b> function during initialization to allow the fax service provider (FSP) to present virtual fax devices. Each FSP that presents virtual fax devices to the fax service must export the <b>FaxDevVirtualDeviceCreation</b> function.


## -parameters




### -param DeviceCount [out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable that receives the number of virtual fax devices the fax service must create for the FSP. If the FSP sets this parameter to zero, the initialization of the provider will fail.


### -param DeviceNamePrefix [out]

Type: <b>LPWSTR</b>

Pointer to a variable that receives a null-terminated Unicode character string, limited to 128 <b>WCHAR</b> characters. The FSP must set this string to the name prefix for the virtual fax device. The fax service appends the value of the <i>DeviceIdPrefix</i>  parameter to this string. The result is a unique device name for each virtual fax device the fax service creates.


### -param DeviceIdPrefix [out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable that receives a nonzero value. The FSP must set this member to a unique numeric value that identifies the virtual fax device. The fax service adds this value to a sequential number, beginning with zero for the first virtual device. The result is a unique device identifier for each virtual fax device the fax service creates.


### -param CompletionPort [in]

Type: <b>HANDLE</b>

Specifies a handle that the FSP must use to post I/O completion port packets to the fax service for asynchronous line status events. Currently the <b>FaxDevVirtualDeviceCreation</b> function supports only the event that signals an incoming call.
                

The completion port packet must be a TAPI 2.x <a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a> structure. The FSP must allocate memory for the structure with <b>LocalAlloc(</b>LPTR, sizeof(LINEMESSAGE)<b>)</b>. The fax service provider must pass the size of the memory allocated (which is sizeof(LINEMESSAGE) in this case) to the <i>dwNumberOfBytesTransferred</i> parameter of the <a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a> method. The fax service frees any memory allocated for the completion packet structure.

The FSP must set the members of the structure as follows.

<table class="clsStd">
<tr>
<th>Member</th>
<th>Contents</th>
</tr>
<tr>
<td><b>hDevice</b></td>
<td>Set to <b>DeviceId</b> from <a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>
</td>
</tr>
<tr>
<td><b>dwMessageID</b></td>
<td>Set to 0</td>
</tr>
<tr>
<td><b>dwCallbackInstance</b></td>
<td>Set to 0</td>
</tr>
<tr>
<td><b>dwParam1</b></td>
<td>Set to LINEDEVSTATE_RINGING</td>
</tr>
<tr>
<td><b>dwParam2</b></td>
<td>Set to 0</td>
</tr>
<tr>
<td><b>dwParam1</b></td>
<td>Set to 0</td>
</tr>
</table>
 

For information about line status events, see <a href="https://msdn.microsoft.com/41e8a777-a57a-4d6c-850f-e21b58081b0d">LINEDEVSTATE_ Constants</a> in the TAPI documentation. For information about I/O completion ports, see <a href="https://msdn.microsoft.com/213c48e8-bb21-43ed-9c00-2a5cf8ac25f0">I/O Completion Ports</a>.


### -param CompletionKey [in]

Type: <b>ULONG_PTR</b>

Specifies a completion key value. The FSP must use this value when the provider posts completion port packets to the fax service. The FSP should pass this opaque value to the <a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The fax service checks the FSP DLL for the <b>FaxDevVirtualDeviceCreation</b> function during initialization. If the FSP exports the function, the fax service assumes that the provider will present virtual fax devices. The fax service handles virtual fax devices the same way it handles physical fax devices. After initialization there is no difference between the functionality or operation of an FSP that presents virtual fax devices, and one that does not present them.

When an FSP uses physical fax devices, the TAPI and the telephony service provider (TSP) enumerate the devices for the fax service. If the FSP does not have physical fax devices, and it presents only virtual fax devices, a TSP will not exist, and TAPI will not enumerate the devices. In this instance, <b>FaxDevVirtualDeviceCreation</b> provides the virtual fax device enumeration for the fax service.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692918(v=VS.85).aspx">Creating a Completion Packet</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684545(v=VS.85).aspx">FaxDevInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a>



<a href="https://msdn.microsoft.com/69a9b1e5-2d40-42de-a14a-f7b6f29bf571">PostQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692954(v=VS.85).aspx">Using a Virtual Device to Transmit a Fax</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693469(v=VS.85).aspx">Virtual Fax Devices</a>
 

 

