---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WSACOMPLETION structure


## -description


The <b>WSACOMPLETION</b> structure specifies completion notification settings for I/O control calls made to a registered namespace.


## -struct-fields




### -field Type

Type: <b>WSACOMPLETIONTYPE</b>

The type of completion notification required. See Remarks.


### -field Parameters

The parameters required to complete the callback. The structures within the Parameters union specify information required for completing the callback of each given type. For example, the <b>WindowMessage</b> structure must be filled  when <b>Type</b> is set to NSP_NOTIFY_HWND.


### -field Parameters.WindowMessage


### -field Parameters.WindowMessage.hWnd

<b>Type: <b>HWND</b>
</b>
Windows handle.


### -field Parameters.WindowMessage.uMsg

<b>Type: <b>UINT</b>
</b>
Message handle.


### -field Parameters.WindowMessage.context

<b>Type: <b>WPARAM</b>
</b>
Context of the message or handle.


### -field Parameters.Event


### -field Parameters.Event.lpOverlapped

<b>Type: <b>LPWSAOVERLAPPED</b>
</b>
A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565952">WSAOVERLAPPED</a> structure.


### -field Parameters.Apc


### -field Parameters.Apc.lpOverlapped

<b>Type: <b>LPWSAOVERLAPPED</b>
</b>
A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565952">WSAOVERLAPPED</a> structure.


### -field Parameters.Apc.lpfnCompletionProc

<b>Type: <b>LPWSAOVERLAPPED_COMPLETION_ROUTINE</b>
</b>
A pointer to an application-provided completion routine.


### -field Parameters.Port


### -field Parameters.Port.lpOverlapped

<b>Type: <b>LPWSAOVERLAPPED</b>
</b>
A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565952">WSAOVERLAPPED</a> structure.


### -field Parameters.Port.hPort

<b>Type: <b>HANDLE</b>
</b>
A handle to the port.


### -field Parameters.Port.Key

<b>Type: <b>ULONG_PTR</b>
</b>
A pointer to the key.


## -remarks



The <b>WSACOMPLETION</b> structure enables callbacks to be provided in any of the following formats, based on the value provided in <b>Type</b>:

<table>
<tr>
<th>Callback Format</th>
<th>Type value</th>
</tr>
<tr>
<td>Polling </td>
<td>NSP_NOTIFY_IMMEDIATELY</td>
</tr>
<tr>
<td>Window Message</td>
<td>NSP_NOTIFY_HWND</td>
</tr>
<tr>
<td>Event</td>
<td>NSP_NOTIFY_EVENT</td>
</tr>
<tr>
<td>APC</td>
<td>NSP_NOTIFY_APC</td>
</tr>
<tr>
<td>Completion Port</td>
<td>NSP_NOTIFY_PORT</td>
</tr>
</table>
 

For a blocking function, set the <b>WSACOMPLETION</b> structure to null.




## -see-also




<a href="https://msdn.microsoft.com/6ecaedf0-0038-46d3-9916-c9cb069c5e92">WSANSPIoctl</a>
 

 

