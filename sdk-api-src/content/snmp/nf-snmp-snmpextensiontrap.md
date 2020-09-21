---
UID: NF:snmp.SnmpExtensionTrap
title: SnmpExtensionTrap function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionTrap function to retrieve information the service needs to generate traps for the SNMP extension agent.
helpviewer_keywords: ["SNMP_GENERICTRAP_AUTHFAILURE","SNMP_GENERICTRAP_COLDSTART","SNMP_GENERICTRAP_EGPNEIGHLOSS","SNMP_GENERICTRAP_ENTERSPECIFIC","SNMP_GENERICTRAP_LINKDOWN","SNMP_GENERICTRAP_LINKUP","SNMP_GENERICTRAP_WARMSTART","SnmpExtensionTrap","SnmpExtensionTrap callback","SnmpExtensionTrap callback function [SNMP]","_snmp_snmpextensiontrap","snmp.snmpextensiontrap","snmp/SnmpExtensionTrap"]
old-location: snmp\snmpextensiontrap.htm
tech.root: SNMP
ms.assetid: 5c768bf5-aa25-4ead-8ee9-fc1f30de4354
ms.date: 12/05/2018
ms.keywords: SNMP_GENERICTRAP_AUTHFAILURE, SNMP_GENERICTRAP_COLDSTART, SNMP_GENERICTRAP_EGPNEIGHLOSS, SNMP_GENERICTRAP_ENTERSPECIFIC, SNMP_GENERICTRAP_LINKDOWN, SNMP_GENERICTRAP_LINKUP, SNMP_GENERICTRAP_WARMSTART, SnmpExtensionTrap, SnmpExtensionTrap callback, SnmpExtensionTrap callback function [SNMP], _snmp_snmpextensiontrap, snmp.snmpextensiontrap, snmp/SnmpExtensionTrap
req.header: snmp.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpExtensionTrap
 - snmp/SnmpExtensionTrap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Snmp.h
api_name:
 - SnmpExtensionTrap
---

# SnmpExtensionTrap function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionTrap</b> function to retrieve information the service needs to generate traps for the SNMP extension agent. The service calls this function only after the extension agent sets the trap event handle to the signaled state during a call to the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a> function. The 
<b>SnmpExtensionTrap</b> function is an element of the SNMP Extension Agent API.

## -parameters

### -param pEnterpriseOid [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the object identifier of the enterprise that generated the trap. The SNMP service does not free the memory for this variable.

### -param pGenericTrapId [out]

Pointer to a variable to receive an indication of the generic trap. This parameter can be one of the following values. 



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
The agent is reinitializing itself but will not alter objects within its view.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_LINKDOWN"></a><a id="snmp_generictrap_linkdown"></a><dl>
<dt><b>SNMP_GENERICTRAP_LINKDOWN</b></dt>
</dl>
</td>
<td width="60%">
An attached interface has changed from the "up" state to the "down" state. The first variable identifies the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_LINKUP"></a><a id="snmp_generictrap_linkup"></a><dl>
<dt><b>SNMP_GENERICTRAP_LINKUP</b></dt>
</dl>
</td>
<td width="60%">
An attached interface has changed from the "down" state to the "up" state. The first variable identifies the interface.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_AUTHFAILURE"></a><a id="snmp_generictrap_authfailure"></a><dl>
<dt><b>SNMP_GENERICTRAP_AUTHFAILURE</b></dt>
</dl>
</td>
<td width="60%">
An SNMP entity has sent an SNMP message, but has falsely claimed to belong to a known community.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></a><a id="snmp_generictrap_egpneighloss"></a><dl>
<dt><b>SNMP_GENERICTRAP_EGPNEIGHLOSS</b></dt>
</dl>
</td>
<td width="60%">
An EGP peer has changed to the down state. The first variable identifies the IP address of the EGP peer.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_GENERICTRAP_ENTERSPECIFIC"></a><a id="snmp_generictrap_enterspecific"></a><dl>
<dt><b>SNMP_GENERICTRAP_ENTERSPECIFIC</b></dt>
</dl>
</td>
<td width="60%">
Signals an extraordinary event that is identified in the <i>pSpecificTrapId</i> parameter.

</td>
</tr>
</table>

### -param pSpecificTrapId [out]

Pointer to a variable to receive an indication of the specific trap generated.

### -param pTimeStamp [out]

Pointer to a variable to receive the time stamp. It is recommended that you initialize this parameter with the value returned by a call to the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcgetuptime">SnmpSvcGetUptime</a> function.

### -param pVarBindList [out]

Pointer to the variable bindings list. The extension agent must allocate the memory for this parameter. The SNMP service frees the memory with a call to the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindlistfree">SnmpUtilVarBindListFree</a> function.

## -returns

If the 
<b>SnmpExtensionTrap</b> function returns a trap, the return value is <b>TRUE</b>. The SNMP service repeatedly calls the function until it returns a value of <b>FALSE</b>. For additional information, see the following Remarks section.

## -remarks

The SNMP service repeatedly calls the 
<b>SnmpExtensionTrap</b> function when the <i>phSubagentTrapEvent</i> event handle is set to the signaled state. This handle is passed back during the call to the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a> entry point function. The 
<b>SnmpExtensionTrap</b> function must return <b>TRUE</b> to indicate that the parameters contain valid data for a single trap. The function must return <b>FALSE</b> to indicate that the parameters do not represent valid trap data, and to stop the service's repeated calls.

Note that after the SNMP service sends a trap, it frees the memory associated with the variable binding list.

It is important to note that earlier documentation stated that the extension agent should dynamically allocate memory for the enterprise object identifier because the SNMP service would attempt to release the memory after sending a trap. The service will not release the memory associated with the enterprise object identifier. It is recommended that you return a pointer to a static 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure instead.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcgetuptime">SnmpSvcGetUptime</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindlistfree">SnmpUtilVarBindListFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>