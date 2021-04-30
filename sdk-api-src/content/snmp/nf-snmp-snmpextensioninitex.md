---
UID: NF:snmp.SnmpExtensionInitEx
title: SnmpExtensionInitEx function (snmp.h)
description: The Microsoft SNMP service calls the SnmpExtensionInitEx function to identify any additional management information base (MIB) subtrees the SNMP extension agent supports. This function is an element of the SNMP Extension Agent API.
helpviewer_keywords: ["SnmpExtensionInitEx","SnmpExtensionInitEx callback","SnmpExtensionInitEx callback function [SNMP]","_snmp_snmpextensioninitex","snmp.snmpextensioninitex","snmp/SnmpExtensionInitEx"]
old-location: snmp\snmpextensioninitex.htm
tech.root: SNMP
ms.assetid: f4e090ca-3f15-4f50-8ea7-92a06868268f
ms.date: 12/05/2018
ms.keywords: SnmpExtensionInitEx, SnmpExtensionInitEx callback, SnmpExtensionInitEx callback function [SNMP], _snmp_snmpextensioninitex, snmp.snmpextensioninitex, snmp/SnmpExtensionInitEx
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
 - SnmpExtensionInitEx
 - snmp/SnmpExtensionInitEx
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
 - SnmpExtensionInitEx
---

# SnmpExtensionInitEx function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft SNMP service calls the 
<b>SnmpExtensionInitEx</b> function to identify any additional management information base (MIB) subtrees the SNMP extension agent supports. This function is an element of the SNMP Extension Agent API.

## -parameters

### -param pNextSupportedRegion [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the next MIB subtree that the extension agent supports.

## -returns

If the <i>pNextSupportedRegion</i> parameter has been initialized with an additional MIB subtree, the return value is <b>TRUE</b>.

If there are no more MIB subtrees to register, the return value is <b>FALSE</b>.

## -remarks

The SNMP service repeatedly calls the 
<b>SnmpExtensionInitEx</b> function entry point so the extension agent can register support for additional MIB subtrees.

The SNMP service makes a copy of the 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure the extension agent returns in the <i>pNextSupportedRegion</i> parameter. The extension agent must allocate and deallocate the resources associated with the original structure. It can do this when the SNMP service calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a> function.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionclose">SnmpExtensionClose</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensioninit">SnmpExtensionInit</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionmonitor">SnmpExtensionMonitor</a>