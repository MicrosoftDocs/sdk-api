---
UID: NF:snmp.SnmpUtilAsnAnyCpy
title: SnmpUtilAsnAnyCpy function (snmp.h)
description: The SnmpUtilAsnAnyCpy function copies the variable pointed to by the pAnySrc parameter to the pAnyDst parameter. The function allocates any necessary memory for the destination's copy. The SnmpUtilAsnAnyCpy function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilAsnAnyCpy","SnmpUtilAsnAnyCpy function [SNMP]","_snmp_snmputilasnanycpy","snmp.snmputilasnanycpy","snmp/SnmpUtilAsnAnyCpy"]
old-location: snmp\snmputilasnanycpy.htm
tech.root: SNMP
ms.assetid: 0a8743da-ef4a-4b00-b9be-5550896d147a
ms.date: 12/05/2018
ms.keywords: SnmpUtilAsnAnyCpy, SnmpUtilAsnAnyCpy function [SNMP], _snmp_snmputilasnanycpy, snmp.snmputilasnanycpy, snmp/SnmpUtilAsnAnyCpy
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
 - SnmpUtilAsnAnyCpy
 - snmp/SnmpUtilAsnAnyCpy
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
 - SnmpUtilAsnAnyCpy
---

# SnmpUtilAsnAnyCpy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilAsnAnyCpy</b> function copies the variable pointed to by the <i>pAnySrc</i> parameter to the <i>pAnyDst</i> parameter. The function allocates any necessary memory for the destination's copy. The 
<b>SnmpUtilAsnAnyCpy</b> function is an element of the SNMP Utility API.

## -parameters

### -param pAnyDst [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a> structure to receive the copy.

### -param pAnySrc [in]

Pointer to an 
<b>AsnAny</b> structure to copy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilasnanyfree">SnmpUtilAsnAnyFree</a> function to free the memory that the 
<b>SnmpUtilAsnAnyCpy</b> function allocates for the destination structure.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnany">AsnAny</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilasnanyfree">SnmpUtilAsnAnyFree</a>