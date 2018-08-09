---
UID: NF:winsnmp.SnmpCreateSession
title: SnmpCreateSession function
author: windows-sdk-content
description: The SnmpCreateSession function requests the Microsoft WinSNMP implementation to open a session for the WinSNMP application.
old-location: snmp\snmpcreatesession.htm
old-project: snmp
ms.assetid: 8d982eb5-a7b5-418e-94ad-3e5dc43d225c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpCreateSession, SnmpCreateSession function [SNMP], _snmp_snmpcreatesession, snmp.snmpcreatesession, winsnmp/SnmpCreateSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsnmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpCreateSession
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpCreateSession function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpCreateSession</b> function requests the Microsoft WinSNMP implementation to open a session for the WinSNMP application. The application can specify how the implementation should inform the WinSNMP session of available SNMP messages and asynchronous events. The application can specify a window notification message or an 
<a href="https://msdn.microsoft.com/9871b4a8-c96c-48a7-9e7e-7fe1c259545e">SNMPAPI_CALLBACK</a> function to notify the session.

The 
<b>SnmpCreateSession</b> function is an element of the WinSNMP API, version 2.0. When developing new WinSNMP applications, it is recommended that you call 
<b>SnmpCreateSession</b> to open a WinSNMP session instead of calling the 
<a href="https://msdn.microsoft.com/45085cad-2bfb-4f6c-9e42-6041fed681b8">SnmpOpen</a> function.


## -parameters




### -param hWnd [in]

Handle to a window of the WinSNMP application to notify when an asynchronous request completes, or when trap notification occurs. This parameter is required for window notification messages for the session.


### -param wMsg [in]

Specifies an unsigned integer that identifies the notification message to send to the WinSNMP application window. This parameter is required for window notification messages for the session.


### -param fCallBack [in]

Specifies the address of an application-defined, session-specific 
<a href="https://msdn.microsoft.com/9871b4a8-c96c-48a7-9e7e-7fe1c259545e">SNMPAPI_CALLBACK</a> function. The implementation will call this function to inform the WinSNMP session when notifications are available. 




This parameter is required to specify callback notifications for the session. This parameter must be <b>NULL</b> to specify window notification messages for the session. For additional information, see the following Remarks section.


### -param lpClientData [in]

Pointer to application-defined data to pass to the callback function specified by the <i>fCallback</i> parameter. This parameter is optional and can be <b>NULL</b>. If the <i>fCallback</i> parameter is <b>NULL</b>, the implementation ignores this parameter.


## -returns



If the function succeeds, the return value is a handle that identifies the WinSNMP session that the implementation opens for the calling application.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function did not complete successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_HWND_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>fCallback</i> parameter is <b>NULL</b>, but the <i>hWnd</i> parameter is not a valid window handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_MESSAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>fCallback</i> parameter is <b>NULL</b>, but the <i>wMsg</i> parameter is not a valid message value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_MODE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>fCallback</i> parameter is <b>NULL</b> and the <i>hWnd</i> and <i>wMsg</i> parameters are valid individually. However, the values are mutually incompatible on the Windows platform.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The combination of parameter values does not specify callback notifications or window notification messages.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>
 




## -remarks



The 
<b>SnmpCreateSession</b> function returns a unique handle to each open WinSNMP session within the calling WinSNMP application. The application must use the session handle that 
<b>SnmpCreateSession</b> returns in other WinSNMP function calls to facilitate allocation and deallocation of resources by the implementation.

It is recommended that a WinSNMP application call the 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> function once for each session that the implementation opens as a result of a call to the 
<b>SnmpCreateSession</b> function. If a WinSNMP application terminates unexpectedly, it must call 
<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a> before it terminates to enable the implementation to deallocate all resources.

<h3><a id="Callback_Notifications"></a><a id="callback_notifications"></a><a id="CALLBACK_NOTIFICATIONS"></a>Callback Notifications</h3>
If the <i>fCallback</i> parameter is not <b>NULL</b> on a successful call to the 
<b>SnmpCreateSession</b> function, the implementation alerts the session to notifications using the callback function specified by the <i>fCallback</i> parameter.

Following is an example of a call to the 
<b>SnmpCreateSession</b> function, requesting that the implementation signal the session about messages and events using callback notifications.

<code>hSession = SnmpCreateSession (0, 0, myFunc, &lt;NULL|myData&gt;);</code>

<h3><a id="Window_Notification_Messages"></a><a id="window_notification_messages"></a><a id="WINDOW_NOTIFICATION_MESSAGES"></a>Window Notification Messages</h3>
The 
<b>SnmpCreateSession</b> function passes to the implementation the handle to an application window and a notification message identifier. When the application window receives the notification message specified by the <i>wMsg</i> parameter, the WinSNMP application must retrieve the incoming protocol data unit (PDU). The application does this by calling the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function with the session handle returned by 
<b>SnmpCreateSession</b>.

One WinSNMP application can open multiple WinSNMP sessions. If an application opens multiple sessions using the same window handle, it is recommended that the WinSNMP application specify a unique <i>wMsg</i> parameter for each session.

Following is an example of a call to the 
<b>SnmpCreateSession</b> function, requesting that the implementation signal the session about messages and events using window notification messages.

<code>hSession = SnmpCreateSession (myWnd, myMsg, NULL, NULL);</code>




## -see-also




<a href="https://msdn.microsoft.com/9871b4a8-c96c-48a7-9e7e-7fe1c259545e">SNMPAPI_CALLBACK</a>



<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a>



<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a>



<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

