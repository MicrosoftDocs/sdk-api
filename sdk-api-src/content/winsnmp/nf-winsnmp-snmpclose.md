---
UID: NF:winsnmp.SnmpClose
title: SnmpClose function (winsnmp.h)
description: The SnmpClose function enables the Microsoft WinSNMP implementation to deallocate memory, resources, and data structures associated with a WinSNMP session.
helpviewer_keywords: ["SnmpClose","SnmpClose function [SNMP]","_snmp_snmpclose","snmp.snmpclose","winsnmp/SnmpClose"]
old-location: snmp\snmpclose.htm
tech.root: SNMP
ms.assetid: eac678f4-c77c-46b5-9c45-62b5822079da
ms.date: 12/05/2018
ms.keywords: SnmpClose, SnmpClose function [SNMP], _snmp_snmpclose, snmp.snmpclose, winsnmp/SnmpClose
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
 - SnmpClose
 - winsnmp/SnmpClose
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
 - SnmpClose
---

# SnmpClose function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpClose</b> function enables the Microsoft WinSNMP implementation to deallocate memory, resources, and data structures associated with a WinSNMP session. The WinSNMP 
<b>SnmpClose</b> function also closes communications mechanisms the implementation opened as a result of a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function.

## -parameters

### -param session [in]

Handle to the WinSNMP session to close.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>session</i> parameter is invalid.

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

It is recommended that a WinSNMP application call the 
<b>SnmpClose</b> function once for each session that the application opened using the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function. If a WinSNMP application terminates unexpectedly, it must call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> before it terminates to enable the implementation to deallocate all resources. The implementation processes one 
<b>SnmpCleanup</b> call as if it were a series of 
<b>SnmpClose</b> calls, one call for each session opened as a result of a call to 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>.

When the implementation closes a session it discards all outstanding incoming and outgoing asynchronous requests and replies for the session. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-sessions">WinSNMP Sessions</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>