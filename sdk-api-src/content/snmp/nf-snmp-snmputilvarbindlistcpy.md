---
UID: NF:snmp.SnmpUtilVarBindListCpy
title: SnmpUtilVarBindListCpy function (snmp.h)
description: The SnmpUtilVarBindListCpy function copies the specified SnmpVarBindList structure, and allocates any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilVarBindListCpy","SnmpUtilVarBindListCpy function [SNMP]","_snmp_snmputilvarbindlistcpy","snmp.snmputilvarbindlistcpy","snmp/SnmpUtilVarBindListCpy"]
old-location: snmp\snmputilvarbindlistcpy.htm
tech.root: SNMP
ms.assetid: 19837eac-c5b0-46a6-b10d-4460cf918cba
ms.date: 12/05/2018
ms.keywords: SnmpUtilVarBindListCpy, SnmpUtilVarBindListCpy function [SNMP], _snmp_snmputilvarbindlistcpy, snmp.snmputilvarbindlistcpy, snmp/SnmpUtilVarBindListCpy
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
 - SnmpUtilVarBindListCpy
 - snmp/SnmpUtilVarBindListCpy
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
 - SnmpUtilVarBindListCpy
---

# SnmpUtilVarBindListCpy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The 
				<b>SnmpUtilVarBindListCpy</b> function copies the specified 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure, and allocates any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.

## -parameters

### -param pVblDst [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure to receive the copy.

### -param pVblSrc [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a> structure to copy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindlistfree">SnmpUtilVarBindListFree</a> function to free memory that the 
<b>SnmpUtilVarBindListCpy</b> function allocates for the destination structure.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidcpy">SnmpUtilOidCpy</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindlistfree">SnmpUtilVarBindListFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbindlist">SnmpVarBindList</a>