---
UID: NF:winsnmp.SnmpGetRetransmitMode
title: SnmpGetRetransmitMode function (winsnmp.h)
description: The WinSNMP SnmpGetRetransmitMode function returns the current setting of the retransmission mode to a WinSNMP application.
helpviewer_keywords: ["SNMPAPI_OFF","SNMPAPI_ON","SnmpGetRetransmitMode","SnmpGetRetransmitMode function [SNMP]","_snmp_snmpgetretransmitmode","snmp.snmpgetretransmitmode","winsnmp/SnmpGetRetransmitMode"]
old-location: snmp\snmpgetretransmitmode.htm
tech.root: SNMP
ms.assetid: 8df40980-56e2-485f-87e0-42878b320e4e
ms.date: 12/05/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpGetRetransmitMode, SnmpGetRetransmitMode function [SNMP], _snmp_snmpgetretransmitmode, snmp.snmpgetretransmitmode, winsnmp/SnmpGetRetransmitMode
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
 - SnmpGetRetransmitMode
 - winsnmp/SnmpGetRetransmitMode
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
 - SnmpGetRetransmitMode
---

# SnmpGetRetransmitMode function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetRetransmitMode</b> function returns the current setting of the retransmission mode to a WinSNMP application. The Microsoft WinSNMP implementation uses the retransmission mode to govern transmission time-outs and retransmission attempts on calls to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function.

## -parameters

### -param nRetransmitMode [out]

Pointer to an unsigned long integer variable to receive the current retransmission mode in effect for the implementation. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_ON"></a><a id="snmpapi_on"></a><dl>
<dt><b>SNMPAPI_ON</b></dt>
</dl>
</td>
<td width="60%">
The implementation is executing the WinSNMP application's retransmission policy.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The implementation is not executing the WinSNMP application's retransmission policy.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. If 
<b>SnmpGetRetransmitMode</b> fails, the value of the <i>nRetransmitMode</i> parameter has no meaning for the application. To get extended error information, call 
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
<b>SnmpGetRetransmitMode</b> function. For additional information, see 
<a href="/windows/desktop/SNMP/about-retransmission">About Retransmission</a> and 
<a href="/windows/desktop/SNMP/managing-the-retransmission-policy">Managing the Retransmission Policy</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretransmitmode">SnmpSetRetransmitMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>