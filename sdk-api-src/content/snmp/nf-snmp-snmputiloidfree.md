---
UID: NF:snmp.SnmpUtilOidFree
title: SnmpUtilOidFree function (snmp.h)
description: The SnmpUtilOidFree function frees the memory allocated for the specified object identifier. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOidFree","SnmpUtilOidFree function [SNMP]","_snmp_snmputiloidfree","snmp.snmputiloidfree","snmp/SnmpUtilOidFree"]
old-location: snmp\snmputiloidfree.htm
tech.root: SNMP
ms.assetid: 8fc44fdf-956a-4102-bcbb-4cd17a73828c
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidFree, SnmpUtilOidFree function [SNMP], _snmp_snmputiloidfree, snmp.snmputiloidfree, snmp/SnmpUtilOidFree
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
 - SnmpUtilOidFree
 - snmp/SnmpUtilOidFree
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
 - SnmpUtilOidFree
---

# SnmpUtilOidFree function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidFree</b> function frees the memory allocated for the specified object identifier. This function is an element of the SNMP Utility API.

## -parameters

### -param pOid [in, out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure whose memory should be freed.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidappend">SnmpUtilOidAppend</a>