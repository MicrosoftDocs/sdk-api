---
UID: NF:snmp.SnmpExtensionClose
title: SnmpExtensionClose function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionClose function to request that the SNMP extension agent deallocate resources and terminate operations. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SnmpExtensionClose","SnmpExtensionClose callback","SnmpExtensionClose callback function [SNMP]","_snmp_snmpextensionclose","snmp.snmpextensionclose","snmp/SnmpExtensionClose"]
old-location: snmp\snmpextensionclose.htm
tech.root: SNMP
ms.assetid: 19fcac27-daa1-40e2-9038-7f03279381f0
ms.date: 12/05/2018
ms.keywords: SnmpExtensionClose, SnmpExtensionClose callback, SnmpExtensionClose callback function [SNMP], _snmp_snmpextensionclose, snmp.snmpextensionclose, snmp/SnmpExtensionClose
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
 - SnmpExtensionClose
 - snmp/SnmpExtensionClose
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
 - SnmpExtensionClose
---

# SnmpExtensionClose function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionClose</b> function to request that the SNMP extension agent deallocate resources and terminate operations. This function is an element of the SNMP Extension Agent API.



## -returns

This callback function does not return a value.

## -remarks

It is not necessary for the extension agent to call its own 
<b>SnmpExtensionClose</b> entry point. This is because the SNMP service calls the extension agent's 
<b>SnmpExtensionClose</b> function when the service unloads the extension agent from the service's address space. The extension agent can clean up allocated resources and terminate services at this time.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninitex">SnmpExtensionInitEx</a>
