---
UID: NS:snmp.SnmpVarBind
title: SnmpVarBind (snmp.h)
description: The SnmpVarBind structure represents an SNMP variable binding. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
helpviewer_keywords: ["SnmpVarBind","SnmpVarBind structure [SNMP]","_snmp_snmpvarbind_str","snmp.snmpvarbind_str","snmp/SnmpVarBind"]
old-location: snmp\snmpvarbind_str.htm
tech.root: SNMP
ms.assetid: 40f9930d-93d1-45eb-aa3a-499947004fcf
ms.date: 12/05/2018
ms.keywords: SnmpVarBind, SnmpVarBind structure [SNMP], _snmp_snmpvarbind_str, snmp.snmpvarbind_str, snmp/SnmpVarBind
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
req.typenames: SnmpVarBind
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpVarBind
 - snmp/SnmpVarBind
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Snmp.h
api_name:
 - SnmpVarBind
---

# SnmpVarBind structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpVarBind</b> structure represents an SNMP variable binding. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API</a> functions.

## -struct-fields

### -field name

Indicates the variable's name, as an object identifier.

### -field value

Contains the variable's value.

## -see-also

<a href="/windows/desktop/SNMP/snmp-structures">SNMP Structures</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>

