---
UID: NF:snmp.SnmpUtilVarBindListFree
title: SnmpUtilVarBindListFree function (snmp.h)
description: The SnmpUtilVarBindListFree function frees the memory allocated for an SnmpVarBindList structure. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilVarBindListFree","SnmpUtilVarBindListFree function [SNMP]","_snmp_snmputilvarbindlistfree","snmp.snmputilvarbindlistfree","snmp/SnmpUtilVarBindListFree"]
old-location: snmp\snmputilvarbindlistfree.htm
tech.root: SNMP
ms.assetid: 79143aaa-26e1-4142-9c67-508d70034de2
ms.date: 12/05/2018
ms.keywords: SnmpUtilVarBindListFree, SnmpUtilVarBindListFree function [SNMP], _snmp_snmputilvarbindlistfree, snmp.snmputilvarbindlistfree, snmp/SnmpUtilVarBindListFree
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
req.lib: Snmpapi.lib
req.dll: Snmpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpUtilVarBindListFree
 - snmp/SnmpUtilVarBindListFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Snmpapi.dll
api_name:
 - SnmpUtilVarBindListFree
---

# SnmpUtilVarBindListFree function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpUtilVarBindListFree</b> function frees the memory allocated for an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure. This function is an element of the SNMP Utility API.

## -parameters

### -param pVbl [in, out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure whose allocated memory should be freed.

## -returns

This function has no return values.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindfree">SnmpUtilVarBindFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>