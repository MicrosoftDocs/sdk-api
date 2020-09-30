---
UID: NF:winsnmp.SnmpSetPort
title: SnmpSetPort function (winsnmp.h)
description: A WinSNMP application calls the SnmpSetPort function to change the port assigned to a destination entity. The SnmpSetPort function is an element of the WinSNMP API, version 2.0.
helpviewer_keywords: ["SnmpSetPort","SnmpSetPort function [SNMP]","_snmp_snmpsetport","snmp.snmpsetport","winsnmp/SnmpSetPort"]
old-location: snmp\snmpsetport.htm
tech.root: SNMP
ms.assetid: 8b495a60-f1ef-4170-bf11-c98bb3dc857b
ms.date: 12/05/2018
ms.keywords: SnmpSetPort, SnmpSetPort function [SNMP], _snmp_snmpsetport, snmp.snmpsetport, winsnmp/SnmpSetPort
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
 - SnmpSetPort
 - winsnmp/SnmpSetPort
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
 - SnmpSetPort
---

# SnmpSetPort function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpSetPort</b> function to change the port assigned to a destination entity. The 
<b>SnmpSetPort</b> function is an element of the WinSNMP API, version 2.0.

## -parameters

### -param hEntity [in]

Handle to a WinSNMP destination entity. This parameter can specify the handle to an entity acting in the role of an SNMP agent application as a result of a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmplisten">SnmpListen</a> function. For more information, see the following Remarks section.

### -param nPort [in]

Specifies an unsigned integer that identifies the new port assignment for the destination entity. If you specify a local address that is busy, or if you specify a remote address that is unavailable, a call to the 
<b>SnmpSetPort</b> function fails.

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
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>hEntity</i> parameter is already functioning in an agent role as the result of a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmplisten">SnmpListen</a> function. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEntity</i> parameter is invalid. This parameter must be a handle returned by a previous call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function.

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

The Microsoft WinSNMP implementation assigns a port to each management entity as a result of a WinSNMP application's call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function. If the SNMPAPI_UNTRANSLATED mode is in effect when the implementation creates an entity, the implementation typically assigns the standard SNMP request port for the respective protocol family to the entity; for example, UDP 161 or IPX 36879. If the SNMPAPI_TRANSLATED mode is in effect, the implementation assigns the port specified for the entity in the WinSNMP database. To retrieve the current entity and context translation mode in effect for the implementation, an application can call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgettranslatemode">SnmpGetTranslateMode</a> function. For more information, see 
<a href="/windows/desktop/SNMP/setting-the-entity-and-context-translation-mode">Setting the Entity and Context Translation Mode</a> and 
<a href="/windows/desktop/SNMP/the-winsnmp-database">The WinSNMP Database</a>.

A call to the 
<b>SnmpSetPort</b> function fails if the entity specified by the <i>hEntity</i> parameter is currently functioning in an agent role. This is because the entity has already been assigned to a port other than the one specified by the <i>nPort</i> parameter. To ensure assignment of an agent application to a specific port, a WinSNMP application can perform the following steps.

<ol>
<li>
Call <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> as follows:

<code>hAgent = SnmpStrToEntity (hSession, &lt;addrString&gt;);</code>

</li>
<li>
Call <b>SnmpSetPort</b> as follows: 

<code>SnmpSetPort (hAgent, &lt;nPort&gt;);</code>

</li>
<li>
Call <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmplisten">SnmpListen</a> as follows:

<code>SnmpListen (hAgent, SNMPAPI_ON);</code>

</li>
</ol>
where &lt;addrString&gt; contains the string representation of an IP address or an IPX address, and &lt;nPort&gt; contains the new port assignment for the agent application.

Note that an IPX address contains a network number that consists of eight hexadecimal digits (zero-filled if necessary); a separator (either ":", "." or " – "); and a node number that consists of 12 hexadecimal digits (zero-filled if necessary)—for example, 00000001:00081A0D01C2. For more information, see 
<a href="/windows/desktop/SNMP/support-for-ipx-address-strings-in-winsnmp">Support for IPX Address Strings in WinSNMP</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgettranslatemode">SnmpGetTranslateMode</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmplisten">SnmpListen</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>