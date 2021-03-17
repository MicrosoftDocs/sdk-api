---
UID: NF:winsnmp.SnmpGetRetry
title: SnmpGetRetry function (winsnmp.h)
description: The WinSNMP SnmpGetRetry function returns the retry count value, in units, for the retransmission of SNMP message requests. The retry count applies to calls that a WinSNMP application makes to the SnmpSendMsg function for a specified management entity.
helpviewer_keywords: ["SnmpGetRetry","SnmpGetRetry function [SNMP]","_snmp_snmpgetretry","snmp.snmpgetretry","winsnmp/SnmpGetRetry"]
old-location: snmp\snmpgetretry.htm
tech.root: SNMP
ms.assetid: 0c01994b-adce-4525-a41c-71cbe2fde2a8
ms.date: 12/05/2018
ms.keywords: SnmpGetRetry, SnmpGetRetry function [SNMP], _snmp_snmpgetretry, snmp.snmpgetretry, winsnmp/SnmpGetRetry
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
 - SnmpGetRetry
 - winsnmp/SnmpGetRetry
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
 - SnmpGetRetry
---

# SnmpGetRetry function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetRetry</b> function returns the retry count value, in units, for the retransmission of SNMP message requests. The retry count applies to calls that a WinSNMP application makes to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function for a specified management entity.

## -parameters

### -param hEntity [in]

Handle to the destination management entity of interest.

### -param nPolicyRetry [out]

Pointer to an unsigned long integer variable to receive the retry count value for the specified management entity. This is a value that the Microsoft WinSNMP implementation stores in a database. If you do not need the information returned in this parameter, <i>nPolicyRetry</i> must be a <b>NULL</b> pointer.

### -param nActualRetry [out]

Pointer to an unsigned long integer variable to receive the last actual or estimated retry count for the destination entity, as reported by the implementation. If you do not need the information returned in this parameter, <i>nActualRetry</i> must be a <b>NULL</b> pointer. If this parameter is a valid pointer, the function returns 0. For additional information, see the following Remarks section.

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
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEntity</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The <i>nPolicyRetry</i> and <i>nActualRetry</i> parameters are both <b>NULL</b>. The operation was not performed.

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

Typically a WinSNMP application, rather than an agent application, calls the 
<b>SnmpGetRetry</b> function.

A WinSNMP application can modify the retry count value with a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretry">SnmpSetRetry</a> function.

The WinSNMP application can monitor the value of the <i>nActualRetry</i> parameter and compare it to the value of the <i>nPolicyRetry</i> parameter to optimize transmission performance. For additional information, see 
<a href="/windows/desktop/SNMP/about-retransmission">About Retransmission</a> and 
<a href="/windows/desktop/SNMP/managing-the-retransmission-policy">Managing the Retransmission Policy</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetretransmitmode">SnmpGetRetransmitMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretransmitmode">SnmpSetRetransmitMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretry">SnmpSetRetry</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>