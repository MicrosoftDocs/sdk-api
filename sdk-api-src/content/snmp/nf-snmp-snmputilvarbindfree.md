---
UID: NF:snmp.SnmpUtilVarBindFree
title: SnmpUtilVarBindFree function (snmp.h)
description: The SnmpUtilVarBindFree function frees the memory allocated for an SnmpVarBind structure. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilVarBindFree","SnmpUtilVarBindFree function [SNMP]","_snmp_snmputilvarbindfree","snmp.snmputilvarbindfree","snmp/SnmpUtilVarBindFree"]
old-location: snmp\snmputilvarbindfree.htm
tech.root: SNMP
ms.assetid: 6e3d0a04-34f8-4342-837d-c0d357a1d1a3
ms.date: 12/05/2018
ms.keywords: SnmpUtilVarBindFree, SnmpUtilVarBindFree function [SNMP], _snmp_snmputilvarbindfree, snmp.snmputilvarbindfree, snmp/SnmpUtilVarBindFree
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
 - SnmpUtilVarBindFree
 - snmp/SnmpUtilVarBindFree
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
 - SnmpUtilVarBindFree
---

# SnmpUtilVarBindFree function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilVarBindFree</b> function frees the memory allocated for an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure. This function is an element of the SNMP Utility API.

## -parameters

### -param pVb [in, out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure whose memory should be freed.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindlistfree">SnmpUtilVarBindListFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a>