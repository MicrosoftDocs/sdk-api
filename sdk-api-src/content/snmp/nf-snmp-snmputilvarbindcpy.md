---
UID: NF:snmp.SnmpUtilVarBindCpy
title: SnmpUtilVarBindCpy function (snmp.h)
description: The SnmpUtilVarBindCpy function copies the specified SnmpVarBind structure, and allocates any memory necessary for the destination structure. The SnmpUtilVarBindCpy function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilVarBindCpy","SnmpUtilVarBindCpy function [SNMP]","_snmp_snmputilvarbindcpy","snmp.snmputilvarbindcpy","snmp/SnmpUtilVarBindCpy"]
old-location: snmp\snmputilvarbindcpy.htm
tech.root: SNMP
ms.assetid: 0a3e1fb8-360d-4bfa-8fa3-8c114b9fd681
ms.date: 12/05/2018
ms.keywords: SnmpUtilVarBindCpy, SnmpUtilVarBindCpy function [SNMP], _snmp_snmputilvarbindcpy, snmp.snmputilvarbindcpy, snmp/SnmpUtilVarBindCpy
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
 - SnmpUtilVarBindCpy
 - snmp/SnmpUtilVarBindCpy
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
 - SnmpUtilVarBindCpy
---

# SnmpUtilVarBindCpy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilVarBindCpy</b> function copies the specified 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure, and allocates any memory necessary for the destination structure. The 
<b>SnmpUtilVarBindCpy</b> function is an element of the SNMP Utility API.

## -parameters

### -param pVbDst [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure to receive the copy.

### -param pVbSrc [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure to copy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindfree">SnmpUtilVarBindFree</a> function to free memory that the 
<b>SnmpUtilVarBindCpy</b> function allocates for the destination structure.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilvarbindfree">SnmpUtilVarBindFree</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a>