---
UID: NF:snmp.SnmpUtilOidCpy
title: SnmpUtilOidCpy function (snmp.h)
description: The SnmpUtilOidCpy function copies the variable pointed to by the pOidSrc parameter to the pOidDst parameter, allocating any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOidCpy","SnmpUtilOidCpy function [SNMP]","_snmp_snmputiloidcpy","snmp.snmputiloidcpy","snmp/SnmpUtilOidCpy"]
old-location: snmp\snmputiloidcpy.htm
tech.root: SNMP
ms.assetid: 65947bdb-1165-4e5d-b3ca-1c54cd50166e
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidCpy, SnmpUtilOidCpy function [SNMP], _snmp_snmputiloidcpy, snmp.snmputiloidcpy, snmp/SnmpUtilOidCpy
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
 - SnmpUtilOidCpy
 - snmp/SnmpUtilOidCpy
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
 - SnmpUtilOidCpy
---

# SnmpUtilOidCpy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidCpy</b> function copies the variable pointed to by the <i>pOidSrc</i> parameter to the <i>pOidDst</i> parameter, allocating any necessary memory for the destination's copy. This function is an element of the SNMP Utility API.

## -parameters

### -param pOidDst [out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the copy.

### -param pOidSrc [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to copy.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a> function to free memory that the 
<b>SnmpUtilOidCpy</b> function allocates for the destination structure.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a>