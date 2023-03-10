---
UID: NF:snmp.SnmpUtilOidToA
title: SnmpUtilOidToA function (snmp.h)
description: The SnmpUtilOidToA function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOidToA","SnmpUtilOidToA function [SNMP]","_snmp_snmputiloidtoa","snmp.snmputiloidtoa","snmp/SnmpUtilOidToA"]
old-location: snmp\snmputiloidtoa.htm
tech.root: SNMP
ms.assetid: c21124ac-f2f8-4096-9100-639ded42d198
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidToA, SnmpUtilOidToA function [SNMP], _snmp_snmputiloidtoa, snmp.snmputiloidtoa, snmp/SnmpUtilOidToA
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
 - SnmpUtilOidToA
 - snmp/SnmpUtilOidToA
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
 - SnmpUtilOidToA
---

# SnmpUtilOidToA function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidToA</b> function converts an object identifier (OID) to a null-terminated string. This function is an element of the SNMP Utility API.

## -parameters

### -param Oid [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to convert.

## -returns

The function returns a null-terminated string of characters that contains the string representation of the object identifier pointed to by the <i>Oid</i> parameter.

## -remarks

The 
<b>SnmpUtilOidToA</b> function can assist with the debugging of SNMP applications.

For more information, see the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilidstoa">SnmpUtilIdsToA</a> function. 
<b>SnmpUtilOidToA</b> calls 
<b>SnmpUtilIdsToA</b> internally to format the string.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilidstoa">SnmpUtilIdsToA</a>