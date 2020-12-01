---
UID: NF:snmp.SnmpUtilPrintOid
title: SnmpUtilPrintOid function (snmp.h)
description: The SnmpUtilPrintOid function formats the specified object identifier (OID) and prints the result to the standard output device. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilPrintOid","SnmpUtilPrintOid function [SNMP]","_snmp_snmputilprintoid","snmp.snmputilprintoid","snmp/SnmpUtilPrintOid"]
old-location: snmp\snmputilprintoid.htm
tech.root: SNMP
ms.assetid: 8d5e9b79-83a5-49ed-8621-f12cbf9c59d0
ms.date: 12/05/2018
ms.keywords: SnmpUtilPrintOid, SnmpUtilPrintOid function [SNMP], _snmp_snmputilprintoid, snmp.snmputilprintoid, snmp/SnmpUtilPrintOid
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
 - SnmpUtilPrintOid
 - snmp/SnmpUtilPrintOid
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
 - SnmpUtilPrintOid
---

# SnmpUtilPrintOid function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilPrintOid</b> function formats the specified object identifier (OID) and prints the result to the standard output device. This function is an element of the SNMP Utility API.

## -parameters

### -param Oid [in]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to print.

## -returns

This function does not return a value.

## -remarks

The 
<b>SnmpUtilPrintOid</b> function can assist with the debugging of command-line SNMP applications. The function prints the object identifier as a sequence of numbers separated by periods ('.'); for example, 1.3.6.1.4.1.311.

## -see-also

<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a>



<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputildbgprint">SnmpUtilDbgPrint</a>