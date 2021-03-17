---
UID: NF:winsnmp.SnmpListen
title: SnmpListen function (winsnmp.h)
description: The WinSNMP SnmpListen function registers a WinSNMP application as an SNMP agent.
helpviewer_keywords: ["SNMPAPI_OFF","SNMPAPI_ON","SnmpListen","SnmpListen function [SNMP]","_snmp_snmplisten","snmp.snmplisten","winsnmp/SnmpListen"]
old-location: snmp\snmplisten.htm
tech.root: SNMP
ms.assetid: e89c9315-efe4-4241-a7c4-f4475b107701
ms.date: 12/05/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpListen, SnmpListen function [SNMP], _snmp_snmplisten, snmp.snmplisten, winsnmp/SnmpListen
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
 - SnmpListen
 - winsnmp/SnmpListen
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
 - SnmpListen
---

# SnmpListen function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpListen</b> function registers a WinSNMP application as an SNMP agent. An agent application calls this function to inform the Microsoft WinSNMP implementation that an entity will be acting in the role of an SNMP agent. An application also calls this function to inform the implementation when an entity will no longer be acting in this role. The 
<b>SnmpListen</b> function is an element of the WinSNMP API, version 2.0.

## -parameters

### -param hEntity [in]

Handle to the WinSNMP entity to notify when the Microsoft WinSNMP implementation receives an incoming SNMP request message (PDU). This parameter identifies the agent application. For more information, see the following Remarks and Return Values sections. 




When you call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function, you can specify whether the implementation should use a window notification message or an 
<a href="/windows/desktop/api/winsnmp/nc-winsnmp-snmpapi_callback">SNMPAPI_CALLBACK</a> function to notify the application when an SNMP message or asynchronous event is available.

### -param lStatus [in]

Specifies an unsigned long integer variable that indicates whether the WinSNMP entity identified by the <i>hEntity</i> parameter is acting in an SNMP agent role, or if it is no longer acting in this role. This parameter can be one of the following values. 



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
The specified WinSNMP entity is functioning in an agent role.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The specified WinSNMP entity is not functioning in an agent role.

</td>
</tr>
</table>
 

Passing a value of SNMPAPI_OFF releases both the resources allocated to the entity and the port assigned it. For more information, see the following Remarks section.

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
The <i>hEntity</i> parameter is invalid. This parameter must be a handle returned by a previous call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_MODE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lStatus</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>hEntity</i> parameter is already functioning in the role of an SNMP agent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_RESOURCE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
There is a network transport layer error. A socket could not be created for the entity specified by the <i>hEntity</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_OTHER</b></dt>
</dl>
</td>
<td width="60%">
An error occurred in the network transport layer while trying to bind a socket for the entity specified by the <i>hEntity</i> parameter.

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

When you specify an entity, you explicitly specify the address family, interface address, and port for the entity. This is because WinSNMP assigns these attributes to each WinSNMP entity as a result of a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a> function. The implementation uses the address and port settings currently assigned to the entity specified by the <i>hEntity</i> parameter when it sends notifications to the agent application. For more information, see 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetport">SnmpSetPort</a>.

When you call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> function for a WinSNMP session and the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> function for a WinSNMP application, you must release all ports associated with WinSNMP agent applications.

For more information about SNMP management applications and agent applications, see 
<a href="/windows/desktop/SNMP/registering-an-snmp-agent-application">Registering an SNMP Agent Application</a> and 
<a href="/windows/desktop/SNMP/about-snmp">About SNMP</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetport">SnmpSetPort</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstrtoentity">SnmpStrToEntity</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>