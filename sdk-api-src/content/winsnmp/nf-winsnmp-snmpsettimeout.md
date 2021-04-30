---
UID: NF:winsnmp.SnmpSetTimeout
title: SnmpSetTimeout function (winsnmp.h)
description: The WinSNMP SnmpSetTimeout function enables a WinSNMP application to change the time-out value for the transmission of SNMP message requests.
helpviewer_keywords: ["SnmpSetTimeout","SnmpSetTimeout function [SNMP]","_snmp_snmpsettimeout","snmp.snmpsettimeout","winsnmp/SnmpSetTimeout"]
old-location: snmp\snmpsettimeout.htm
tech.root: SNMP
ms.assetid: ae72f775-9f2a-4c16-b866-14ab17fd3a6a
ms.date: 12/05/2018
ms.keywords: SnmpSetTimeout, SnmpSetTimeout function [SNMP], _snmp_snmpsettimeout, snmp.snmpsettimeout, winsnmp/SnmpSetTimeout
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
 - SnmpSetTimeout
 - winsnmp/SnmpSetTimeout
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
 - SnmpSetTimeout
---

# SnmpSetTimeout function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetTimeout</b> function enables a WinSNMP application to change the time-out value for the transmission of SNMP message requests. The time-out value applies to calls that a WinSNMP application makes to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function for a specified management entity. The Microsoft WinSNMP implementation stores the value in a database.

## -parameters

### -param hEntity [in]

Handle to the destination management entity of interest.

### -param nPolicyTimeout [in]

Specifies a new time-out value, in hundredths of a second, for the management entity. This value replaces the value currently stored in the implementation's database. 




If this parameter is equal to zero, and the current retransmission mode is equal to SNMPAPI_ON, the implementation selects a time-out value. The implementation uses this time-out value when it executes the WinSNMP application's retransmission policy.

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
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

Typically a WinSNMP manager application, rather than an agent application, calls the 
<b>SnmpSetTimeout</b> function.

For additional information, see 
<a href="/windows/desktop/SNMP/about-retransmission">About Retransmission</a> and 
<a href="/windows/desktop/SNMP/managing-the-retransmission-policy">Managing the Retransmission Policy</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetretransmitmode">SnmpGetRetransmitMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgettimeout">SnmpGetTimeout</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretransmitmode">SnmpSetRetransmitMode</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>