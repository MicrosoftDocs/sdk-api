---
UID: NF:snmp.SnmpExtensionInit
title: SnmpExtensionInit function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionInit function to initialize the SNMP extension agent DLL. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SnmpExtensionInit","SnmpExtensionInit callback","SnmpExtensionInit callback function [SNMP]","_snmp_snmpextensioninit","snmp.snmpextensioninit","snmp/SnmpExtensionInit"]
old-location: snmp\snmpextensioninit.htm
tech.root: SNMP
ms.assetid: 015f2be2-8e10-4abd-afd0-f76834856733
ms.date: 12/05/2018
ms.keywords: SnmpExtensionInit, SnmpExtensionInit callback, SnmpExtensionInit callback function [SNMP], _snmp_snmpextensioninit, snmp.snmpextensioninit, snmp/SnmpExtensionInit
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
 - SnmpExtensionInit
 - snmp/SnmpExtensionInit
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
 - SnmpExtensionInit
---

# SnmpExtensionInit function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionInit</b> function to initialize the SNMP extension agent DLL. This function is an element of the SNMP Extension Agent API.

## -parameters

### -param dwUptimeReference [in]

Specifies a time-zero reference for the extension agent. 




<div class="alert"><b>Note</b>  Extension agents should ignore this parameter. The SNMP extension agent DLL should use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcgetuptime">SnmpSvcGetUptime</a> function to retrieve the number of centiseconds the SNMP service has been running. For more information, see the following Remarks section.</div>
<div> </div>

### -param phSubagentTrapEvent [out]

Pointer to an event handle the extension agent passes back to the SNMP service. This handle is used to notify the service that the extension agent has one or more traps to send. For additional information about allocating and deallocating the event handle, see the following Remarks section.

### -param pFirstSupportedRegion [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the first MIB subtree that the extension agent supports. For additional information about allocating and deallocating resources for this structure, see the following Remarks section. 




The extension agent can register additional MIB subtrees by implementing the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninitex">SnmpExtensionInitEx</a> entry point function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

Extension agents should ignore the <i>dwUptimeReference</i> parameter. Instead, they should call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcgetuptime">SnmpSvcGetUptime</a> function to retrieve the number of centiseconds that the Microsoft SNMP service has been running. Because the <i>dwUptimeReference</i> parameter stores the elapsed time as a <b>DWORD</b> value in milliseconds, the time can wrap to zero and reflect an inaccurate time interval.

The extension agent notifies the SNMP service that it needs to send one or more traps by setting the event handle passed back in the <i>phSubagentTrapEvent</i> parameter to the signaled state. After this event has been signaled, the SNMP service repeatedly calls the extension agent's 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensiontrap">SnmpExtensionTrap</a> entry point until the function returns a value of <b>FALSE</b>. This indicates that the extension agent has no more traps to send. If the extension agent does not generate traps, the <i>phSubagentTrapEvent</i> parameter should return a value of <b>NULL</b>.

The SNMP extension agent must allocate and deallocate resources for the trap event handle. When the SNMP service calls the 
<b>SnmpExtensionInit</b> function, the extension agent must call the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to allocate the event handle. The extension agent passes the handle to the SNMP service in the <i>phSubagentTrapEvent</i> parameter. When the SNMP service calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a> function, the extension agent must deallocate resources for the trap event handle.

The SNMP service makes a copy of the 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure the extension agent returns in the <i>pFirstSupportedRegion</i> parameter. The extension agent must allocate and deallocate the resources associated with the original structure. It can do this when the SNMP service calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a> function.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionmonitor">SnmpExtensionMonitor</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensiontrap">SnmpExtensionTrap</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpsvcgetuptime">SnmpSvcGetUptime</a>