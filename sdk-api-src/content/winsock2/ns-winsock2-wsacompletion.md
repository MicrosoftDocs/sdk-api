---
UID: NS:winsock2._WSACOMPLETION
title: WSACOMPLETION (winsock2.h)
description: Specifies completion notification settings for I/O control calls made to a registered namespace.
helpviewer_keywords: ["*LPWSACOMPLETION","*PWSACOMPLETION","WSACOMPLETION","WSACOMPLETION structure [Winsock]","winsock.wsacompletion","winsock2/WSACOMPLETION"]
old-location: winsock\wsacompletion.htm
tech.root: WinSock
ms.assetid: 5af4b4d1-6dcb-4fc8-a730-53a8cb92fee4
ms.date: 12/05/2018
ms.keywords: '*LPWSACOMPLETION, *PWSACOMPLETION, WSACOMPLETION, WSACOMPLETION structure [Winsock], winsock.wsacompletion, winsock2/WSACOMPLETION'
f1_keywords:
- winsock2/WSACOMPLETION
dev_langs:
- c++
req.header: winsock2.h
req.include-header: 
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
- Winsock2.h
api_name:
- WSACOMPLETION
targetos: Windows
req.typenames: WSACOMPLETION, *PWSACOMPLETION, *LPWSACOMPLETION
req.redist: 
ms.custom: 19H1
---

# WSACOMPLETION structure


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
A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.


### -field Parameters.Apc


### -field Parameters.Apc.lpOverlapped

<b>Type: <b>LPWSAOVERLAPPED</b>
</b>
A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.


### -field Parameters.Apc.lpfnCompletionProc

<b>Type: <b>LPWSAOVERLAPPED_COMPLETION_ROUTINE</b>
</b>
A pointer to an application-provided completion routine.


### -field Parameters.Port


### -field Parameters.Port.lpOverlapped

<b>Type: <b>LPWSAOVERLAPPED</b>
</b>
A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped">WSAOVERLAPPED</a> structure.


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




<a href="https://docs.microsoft.com/windows/desktop/api/winsock2/nf-winsock2-wsanspioctl">WSANSPIoctl</a>
 

 

