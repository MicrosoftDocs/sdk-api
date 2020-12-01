---
UID: NF:mgmtapi.SnmpMgrGetTrapEx
title: SnmpMgrGetTrapEx function (mgmtapi.h)
description: The SnmpMgrGetTrapEx function returns outstanding trap data that the caller has not received if trap reception is enabled.
helpviewer_keywords: ["SNMP_GENERICTRAP_AUTHFAILURE","SNMP_GENERICTRAP_COLDSTART","SNMP_GENERICTRAP_EGPNEIGHLOSS","SNMP_GENERICTRAP_ENTERSPECIFIC","SNMP_GENERICTRAP_LINKDOWN","SNMP_GENERICTRAP_LINKUP","SNMP_GENERICTRAP_WARMSTART","SnmpMgrGetTrapEx","SnmpMgrGetTrapEx function [SNMP]","_snmp_snmpmgrgettrapex","mgmtapi/SnmpMgrGetTrapEx","snmp.snmpmgrgettrapex"]
old-location: snmp\snmpmgrgettrapex.htm
tech.root: SNMP
ms.assetid: 1dc4b432-8418-46a7-9ea8-5025799c8ec9
ms.date: 12/05/2018
ms.keywords: SNMP_GENERICTRAP_AUTHFAILURE, SNMP_GENERICTRAP_COLDSTART, SNMP_GENERICTRAP_EGPNEIGHLOSS, SNMP_GENERICTRAP_ENTERSPECIFIC, SNMP_GENERICTRAP_LINKDOWN, SNMP_GENERICTRAP_LINKUP, SNMP_GENERICTRAP_WARMSTART, SnmpMgrGetTrapEx, SnmpMgrGetTrapEx function [SNMP], _snmp_snmpmgrgettrapex, mgmtapi/SnmpMgrGetTrapEx, snmp.snmpmgrgettrapex
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
 - SnmpMgrGetTrapEx
 - mgmtapi/SnmpMgrGetTrapEx
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
 - SnmpMgrGetTrapEx
---

# SnmpMgrGetTrapEx function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrGetTrapEx</b> function returns outstanding trap data that the caller has not received if trap reception is enabled. In addition to the information that is returned by the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrgettrap">SnmpMgrGetTrap</a> function, this extended function returns the address of the transport source and the community string of the trap. This function is an element of the SNMP Management API.

## -parameters

### -param enterprise [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the enterprise that generated the SNMP trap.

### -param agentAddress [out]

Pointer to a variable to receive the address of the agent that generated the SNMP trap; this information is retrieved from the SNMP protocol data unit (PDU).

### -param sourceAddress [out]

Pointer to a variable to receive the address of the agent that generated the SNMP trap; this information is retrieved from the network transport.

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
An attached interface has changed from the up state to the down state. The first variable in the variable bindings list identifies the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_LINKUP"></a><a id="snmp_generictrap_linkup"></a><dl>
<dt><b>SNMP_GENERICTRAP_LINKUP</b></dt>
</dl>
</td>
<td width="60%">
An attached interface has changed from the down state to the up state. The first variable in the variable bindings list identifies the interface.

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
An EGP peer has changed to the down state. The first variable in the variable bindings list identifies the IP address of the EGP peer.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_ENTERSPECIFIC"></a><a id="snmp_generictrap_enterspecific"></a><dl>
<dt><b>SNMP_GENERICTRAP_ENTERSPECIFIC</b></dt>
</dl>
</td>
<td width="60%">
An extraordinary event has occurred. It is identified in the <i>specificTrap</i> parameter with an enterprise-specific value.

</td>
</tr>
</table>

### -param specificTrap [out]

Pointer to a variable to receive an indicator of the specific trap generated.

### -param community [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a> structure to receive the community string of the generated SNMP trap.

### -param timeStamp [out]

Pointer to a variable to receive the time stamp.

### -param variableBindings [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure to receive the variable bindings list.

## -returns

If the function returns a trap, the return value is nonzero.

You should call the 
<b>SnmpMgrGetTrapEx</b> function repeatedly until it returns zero. The function may also return the following error codes.

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
Indicates that errors were encountered; traps are not accessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MGMTAPI_NOTRAPS</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no traps are available.

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
<b>SnmpMgrGetTrapEx</b> function. This is because the event handle that is pointed to by the <i>phTrapAvailable</i> parameter of the 
<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a> function enables the event-driven acquisition of SNMP traps. The SNMP Management API signals an application event when the SNMP Trap Service delivers a trap.

The application can also poll the 
<b>SnmpMgrGetTrapEx</b> function for traps at regular intervals. In this case, the application should repeatedly call 
<b>SnmpMgrGetTrapEx</b> until the function returns zero.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/api/snmp/ns-snmp-asnoctetstring">AsnOctetString</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/mgmtapi/nf-mgmtapi-snmpmgrtraplisten">SnmpMgrTrapListen</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>