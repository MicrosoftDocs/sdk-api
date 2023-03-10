---
UID: NS:snmp.SnmpVarBindList
title: SnmpVarBindList (snmp.h)
description: The SnmpVarBindList structure represents an SNMP variable bindings list. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
helpviewer_keywords: ["SnmpVarBindList","SnmpVarBindList structure [SNMP]","_snmp_snmpvarbindlist_str","snmp.snmpvarbindlist_str","snmp/SnmpVarBindList"]
old-location: snmp\snmpvarbindlist_str.htm
tech.root: SNMP
ms.assetid: 73e33a64-39fb-4e36-8267-88c78ec27e26
ms.date: 12/05/2018
ms.keywords: SnmpVarBindList, SnmpVarBindList structure [SNMP], _snmp_snmpvarbindlist_str, snmp.snmpvarbindlist_str, snmp/SnmpVarBindList
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
req.typenames: SnmpVarBindList
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpVarBindList
 - snmp/SnmpVarBindList
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
 - SnmpVarBindList
---

# SnmpVarBindList structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpVarBindList</b> structure represents an SNMP variable bindings list. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API</a> functions.

## -struct-fields

### -field list

A pointer that references an array to access individual variable bindings.

### -field len

Contains the number of variable bindings in the list.

## -see-also

<a href="/windows/desktop/SNMP/snmp-structures">SNMP Structures</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a>

