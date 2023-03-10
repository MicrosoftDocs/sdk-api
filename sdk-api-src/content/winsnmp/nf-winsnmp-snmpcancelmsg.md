---
UID: NF:winsnmp.SnmpCancelMsg
title: SnmpCancelMsg function (winsnmp.h)
description: A WinSNMP application calls the SnmpCancelMsg function to request that the Microsoft WinSNMP implementation cancel retransmission attempts and time-out notifications for an SNMP request message.
helpviewer_keywords: ["SnmpCancelMsg","SnmpCancelMsg function [SNMP]","_snmp_snmpcancelmsg","snmp.snmpcancelmsg","winsnmp/SnmpCancelMsg"]
old-location: snmp\snmpcancelmsg.htm
tech.root: SNMP
ms.assetid: 018ad1b6-6f59-4c5d-813b-734ec8ced28a
ms.date: 12/05/2018
ms.keywords: SnmpCancelMsg, SnmpCancelMsg function [SNMP], _snmp_snmpcancelmsg, snmp.snmpcancelmsg, winsnmp/SnmpCancelMsg
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
 - SnmpCancelMsg
 - winsnmp/SnmpCancelMsg
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
 - SnmpCancelMsg
---

# SnmpCancelMsg function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpCancelMsg</b> function to request that the Microsoft WinSNMP implementation cancel retransmission attempts and time-out notifications for an SNMP request message. The 
<b>SnmpCancelMsg</b> function is an element of the WinSNMP API, version 2.0.

## -parameters

### -param session [in]

Handle to the WinSNMP session that submitted the SNMP request message (PDU) to be canceled.

### -param reqId [in]

Specifies a unique numeric value that identifies the PDU of interest. This parameter must match the request identifier (<b>request_id</b>) of the <i>PDU</i> parameter specified in the application's initial call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>reqId</i> parameter does not identify an outstanding message for the specified session.

</td>
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

Calling the 
<b>SnmpCancelMsg</b> function is equivalent to calling the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretransmitmode">SnmpSetRetransmitMode</a> function, for a specific SNMP message, with the retransmission mode equal to SNMPAPI_OFF.

For more information, see 
<a href="/windows/desktop/SNMP/canceling-retransmission">Canceling Retransmission</a> and 
<a href="/windows/desktop/SNMP/managing-the-retransmission-policy">Managing the Retransmission Policy</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetretransmitmode">SnmpSetRetransmitMode</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>