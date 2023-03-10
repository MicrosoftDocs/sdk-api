---
UID: NF:mgmtapi.SnmpMgrGetTrap
title: SnmpMgrGetTrap function (mgmtapi.h)
description: The SnmpMgrGetTrap function returns outstanding trap data that the caller has not received if trap reception is enabled. This function is an element of the SNMP Management API.
helpviewer_keywords: ["SNMP_GENERICTRAP_AUTHFAILURE","SNMP_GENERICTRAP_COLDSTART","SNMP_GENERICTRAP_EGPNEIGHLOSS","SNMP_GENERICTRAP_ENTERSPECIFIC","SNMP_GENERICTRAP_LINKDOWN","SNMP_GENERICTRAP_LINKUP","SNMP_GENERICTRAP_WARMSTART","SnmpMgrGetTrap","SnmpMgrGetTrap function [SNMP]","_snmp_snmpmgrgettrap","mgmtapi/SnmpMgrGetTrap","snmp.snmpmgrgettrap"]
old-location: snmp\snmpmgrgettrap.htm
tech.root: SNMP
ms.assetid: ce773bbe-0a05-45b5-af80-fc594a83b87a
ms.date: 12/05/2018
ms.keywords: SNMP_GENERICTRAP_AUTHFAILURE, SNMP_GENERICTRAP_COLDSTART, SNMP_GENERICTRAP_EGPNEIGHLOSS, SNMP_GENERICTRAP_ENTERSPECIFIC, SNMP_GENERICTRAP_LINKDOWN, SNMP_GENERICTRAP_LINKUP, SNMP_GENERICTRAP_WARMSTART, SnmpMgrGetTrap, SnmpMgrGetTrap function [SNMP], _snmp_snmpmgrgettrap, mgmtapi/SnmpMgrGetTrap, snmp.snmpmgrgettrap
req.header: mgmtapi.h
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
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpMgrGetTrap
 - mgmtapi/SnmpMgrGetTrap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mgmtapi.dll
api_name:
 - SnmpMgrGetTrap
---

# SnmpMgrGetTrap function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrGetTrap</b> function returns outstanding trap data that the caller has not received if trap reception is enabled. This function is an element of the SNMP Management API.

In addition to the information returned by this function, the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrgettrapex">SnmpMgrGetTrapEx</a> function returns the address of the transport source and the community string of the trap.

## -parameters

### -param enterprise [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the enterprise that generated the SNMP trap.

### -param IPAddress [out]

Pointer to a variable to receive the address of the agent that generated the SNMP trap.

### -param genericTrap [out]

Pointer to a variable to receive an indicator of the generic trap. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_COLDSTART"></a><a id="snmp_generictrap_coldstart"></a><dl>
<dt><b>SNMP_GENERICTRAP_COLDSTART</b></dt>
</dl>
</td>
<td width="60%">
The agent is initializing protocol entities on the managed mode. It may alter objects in its view.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_WARMSTART"></a><a id="snmp_generictrap_warmstart"></a><dl>
<dt><b>SNMP_GENERICTRAP_WARMSTART</b></dt>
</dl>
</td>
<td width="60%">
The agent is reinitializing itself but it will not alter objects in its view.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_LINKDOWN"></a><a id="snmp_generictrap_linkdown"></a><dl>
<dt><b>SNMP_GENERICTRAP_LINKDOWN</b></dt>
</dl>
</td>
<td width="60%">
An attached interface has changed from the "up" state to the "down" state. The first variable in the variable bindings list identifies the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_LINKUP"></a><a id="snmp_generictrap_linkup"></a><dl>
<dt><b>SNMP_GENERICTRAP_LINKUP</b></dt>
</dl>
</td>
<td width="60%">
An attached interface has changed from the "down" state to the "up" state. The first variable in the variable bindings list identifies the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_AUTHFAILURE"></a><a id="snmp_generictrap_authfailure"></a><dl>
<dt><b>SNMP_GENERICTRAP_AUTHFAILURE</b></dt>
</dl>
</td>
<td width="60%">
An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></a><a id="snmp_generictrap_egpneighloss"></a><dl>
<dt><b>SNMP_GENERICTRAP_EGPNEIGHLOSS</b></dt>
</dl>
</td>
<td width="60%">
An EGP peer has changed to the "down" state. The first variable in the variable bindings list identifies the IP address of the EGP peer.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_ENTERSPECIFIC"></a><a id="snmp_generictrap_enterspecific"></a><dl>
<dt><b>SNMP_GENERICTRAP_ENTERSPECIFIC</b></dt>
</dl>
</td>
<td width="60%">
An extraordinary event has occurred and it is identified in the <i>specificTrap</i> parameter with an enterprise-specific value.

</td>
</tr>
</table>

### -param specificTrap [out]

Pointer to a variable to receive an indication of the specific trap generated.

### -param timeStamp [out]

Pointer to a variable to receive the time stamp.

### -param variableBindings [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure to receive the variable bindings list.

## -returns

If the function returns a trap, the return value is <b>TRUE</b>. The code for the error can be retrieved by calling <a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> immediately after the call.

You should call the 
<b>SnmpMgrGetTrap</b> function repeatedly until it returns <b>FALSE</b> (zero). The function may also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_TRAP_ERRORS</b></dt>
</dl>
</td>
<td width="60%">
Indicates errors were encountered; traps are not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_NOTRAPS</b></dt>
</dl>
</td>
<td width="60%">
Indicates no traps are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MEM_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicates a memory allocation error.

</td>
</tr>
</table>

## -remarks

The application must always call the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a> function before calling the 
<b>SnmpMgrGetTrap</b> function. This is because the event handle pointed to by the <i>phTrapAvailable</i> parameter of the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a> function enables the event-driven acquisition of SNMP traps. The SNMP Management API signals an application's event when the SNMP Trap Service delivers a trap.

The application can also poll the 
<b>SnmpMgrGetTrap</b> function for traps at regular intervals. In this case, the application should repeatedly call 
<b>SnmpMgrGetTrap</b> until the function returns zero.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>