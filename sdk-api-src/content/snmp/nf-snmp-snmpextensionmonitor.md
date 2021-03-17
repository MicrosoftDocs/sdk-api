---
UID: NF:snmp.SnmpExtensionMonitor
title: SnmpExtensionMonitor function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionMonitor function to provide the SNMP extension agent with a view to the service's internal counters and parameters. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SnmpExtensionMonitor","SnmpExtensionMonitor callback","SnmpExtensionMonitor callback function [SNMP]","_snmp_snmpextensionmonitor","snmp.snmpextensionmonitor","snmp/SnmpExtensionMonitor"]
old-location: snmp\snmpextensionmonitor.htm
tech.root: SNMP
ms.assetid: 40468bf2-0e91-448b-a2e5-b84b786c67a2
ms.date: 12/05/2018
ms.keywords: SnmpExtensionMonitor, SnmpExtensionMonitor callback, SnmpExtensionMonitor callback function [SNMP], _snmp_snmpextensionmonitor, snmp.snmpextensionmonitor, snmp/SnmpExtensionMonitor
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
 - SnmpExtensionMonitor
 - snmp/SnmpExtensionMonitor
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
 - SnmpExtensionMonitor
---

# SnmpExtensionMonitor function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionMonitor</b> function to provide the SNMP extension agent with a view to the service's internal counters and parameters. This function is an element of the SNMP Extension Agent API.

The 
<b>SnmpExtensionMonitor</b> function is optional. Extension agents should implement the function if they are interested in a view of the SNMP service's internal management objects, as defined in RFC 1213, "Management Information Base for Network Management of TCP/IP-based internets: MIB-II."

## -parameters

### -param pAgentMgmtData [in]

Pointer to an array of 
<a href="/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a> objects (structures). The number of objects, and the type and description of each object, are in accordance with RFC 1213. For more information, see the following Remarks section.

## -returns

Unless an unexpected error occurs while the SNMP extension agent is processing the value of the <i>pAgentMgmtData</i> parameter, the extension agent should return <b>TRUE</b>. If the extension agent returns <b>FALSE</b>, the SNMP service does not load the extension agent, and the service stops directing SNMP requests to the extension agent.

## -remarks

If the extension agent exports the 
<b>SnmpExtensionMonitor</b> function, the SNMP service calls the function during initialization of the extension agent, immediately after the service calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a> and the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninitex">SnmpExtensionInitEx</a> functions.

The SNMP service dynamically updates the SNMP counters (for example, the snmpInPkts and the snmpOutNoSuchNames counters) in the array pointed to by the <i>pAgentMgmtData</i> parameter. In order to be able to read these values while the SNMP service is running, the extension agent must store the pointer to <i>pAgentMgmtData</i>.

Note that an SNMP extension agent should not update the memory pointed to by the <i>pAgentMgmtData</i> parameter. This is because the values of the SNMP service's internal counters would no longer be valid, and the behavior of the SNMP service could become unpredictable. As long as the extension agent does not alter it, the memory pointed to by <i>pAgentMgmtData</i> is valid while the SNMP service is running.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninitex">SnmpExtensionInitEx</a>