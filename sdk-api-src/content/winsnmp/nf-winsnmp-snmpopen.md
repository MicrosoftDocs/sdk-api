---
UID: NF:winsnmp.SnmpOpen
title: SnmpOpen function (winsnmp.h)
description: The SnmpOpen function requests the Microsoft WinSNMP implementation to open a session for the WinSNMP application.
helpviewer_keywords: ["SnmpOpen","SnmpOpen function [SNMP]","_snmp_snmpopen","snmp.snmpopen","winsnmp/SnmpOpen"]
old-location: snmp\snmpopen.htm
tech.root: SNMP
ms.assetid: 45085cad-2bfb-4f6c-9e42-6041fed681b8
ms.date: 12/05/2018
ms.keywords: SnmpOpen, SnmpOpen function [SNMP], _snmp_snmpopen, snmp.snmpopen, winsnmp/SnmpOpen
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
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpOpen
 - winsnmp/SnmpOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpOpen
---

# SnmpOpen function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpOpen</b> function requests the Microsoft WinSNMP implementation to open a session for the WinSNMP application. This WinSNMP function enables the implementation to allocate and initialize memory, resources, data structures, and communications mechanisms. The 
<b>SnmpOpen</b> function returns a handle to the new WinSNMP session.
<div class="alert"><b>Note</b>  When developing new WinSNMP applications, it is recommended that you call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function to open a WinSNMP session instead of calling the 
<b>SnmpOpen</b> function.</div><div> </div>

## -parameters

### -param hWnd [in]

Handle to a window of the WinSNMP application to notify when an asynchronous request completes, or when trap notification occurs.

### -param wMsg [in]

Specifies an unsigned integer that identifies the notification message to send to the WinSNMP application window.

## -returns

If the function succeeds, the return value is a handle that identifies the WinSNMP session that the implementation opens for the calling application.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
The <i>hWnd</i> parameter is not a valid window handle.

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
<b>SnmpOpen</b> function returns a unique handle to each open WinSNMP session within the calling WinSNMP application. The application must use the session handle that 
<b>SnmpOpen</b> returns in other WinSNMP function calls to facilitate allocation and deallocation of resources by the implementation. When the implementation allocates resources to an individual session, it performs an orderly release of resources in response to a call to 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> for the session.

The 
<b>SnmpOpen</b> function passes to the implementation the handle to an application window and a notification message identifier. If the <i>wParam</i> component of the notification message specified by the <i>wMsg</i> parameter is equal to zero, the WinSNMP application must retrieve the incoming protocol data unit (PDU). The application does this by calling the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a> function with the session handle returned by 
<b>SnmpOpen</b>. If the <i>wParam</i> parameter of the notification message is not equal to zero, it represents a WinSNMP error code. The error code applies to the PDU identified by the request identifier in the <i>lParam</i> parameter of the notification message.

One WinSNMP application can open multiple WinSNMP sessions. If an application opens multiple sessions using the same window handle, it is recommended that the WinSNMP application specify a unique <i>wMsg</i> parameter for each session.

It is recommended that a WinSNMP application call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function once for each session that the implementation opens as a result of a call to the 
<b>SnmpOpen</b> function. If a WinSNMP application terminates unexpectedly, it must call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> before it terminates to enable the implementation to deallocate all resources. The implementation treats one 
<b>SnmpCleanup</b> call as if it were a series of 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> calls, one call for each session the implementation opens as a result of a call to 
<b>SnmpOpen</b>.

For information about opening a WinSNMP session and specifying the method used to inform the session of available SNMP messages and asynchronous events, see 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>. When you call 
<b>SnmpCreateSession</b> you can specify a window notification message or an 
<a href="/windows/desktop/api/winsnmp/nc-winsnmp-snmpapi_callback">SNMPAPI_CALLBACK</a> function to notify the session.

For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-sessions">WinSNMP Sessions</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nc-winsnmp-snmpapi_callback">SNMPAPI_CALLBACK</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>