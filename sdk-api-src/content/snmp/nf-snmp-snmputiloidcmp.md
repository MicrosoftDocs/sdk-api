---
UID: NF:snmp.SnmpUtilOidCmp
title: SnmpUtilOidCmp function (snmp.h)
description: The SnmpUtilOidCmp function compares two object identifiers. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOidCmp","SnmpUtilOidCmp function [SNMP]","_snmp_snmputiloidcmp","snmp.snmputiloidcmp","snmp/SnmpUtilOidCmp"]
old-location: snmp\snmputiloidcmp.htm
tech.root: SNMP
ms.assetid: c6ec4984-d984-4642-b110-fd9c2c7e3c5d
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidCmp, SnmpUtilOidCmp function [SNMP], _snmp_snmputiloidcmp, snmp.snmputiloidcmp, snmp/SnmpUtilOidCmp
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
 - SnmpUtilOidCmp
 - snmp/SnmpUtilOidCmp
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
 - SnmpUtilOidCmp
---

# SnmpUtilOidCmp function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidCmp</b> function compares two object identifiers. This function is an element of the SNMP Utility API.

## -parameters

### -param pOid1 [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to compare.

### -param pOid2 [in]

Pointer to a second 
<b>AsnObjectIdentifier</b> structure to compare.

## -returns

The function returns a value greater than zero if <i>pOid1</i> is greater than <i>pOid2</i>, zero if <i>pOid1</i> equals <i>pOid2</i>, and less than zero if <i>pOid1</i> is less than <i>pOid2</i>.

## -remarks

The 
<b>SnmpUtilOidCmp</b> function calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidncmp">SnmpUtilOidNCmp</a> function.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidncmp">SnmpUtilOidNCmp</a>