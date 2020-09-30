---
UID: NF:snmp.SnmpUtilMemFree
title: SnmpUtilMemFree function (snmp.h)
description: The SnmpUtilMemFree function frees the specified memory object. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilMemFree","SnmpUtilMemFree function [SNMP]","_snmp_snmputilmemfree","snmp.snmputilmemfree","snmp/SnmpUtilMemFree"]
old-location: snmp\snmputilmemfree.htm
tech.root: SNMP
ms.assetid: 57cf0398-d2c1-4dd9-ad77-0c453412034a
ms.date: 12/05/2018
ms.keywords: SnmpUtilMemFree, SnmpUtilMemFree function [SNMP], _snmp_snmputilmemfree, snmp.snmputilmemfree, snmp/SnmpUtilMemFree
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
 - SnmpUtilMemFree
 - snmp/SnmpUtilMemFree
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
 - SnmpUtilMemFree
---

# SnmpUtilMemFree function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilMemFree</b> function frees the specified memory object. This function is an element of the SNMP Utility API.

## -parameters

### -param pMem [in, out]

Pointer to the memory object to release.

## -returns

This function does not return a value.

## -remarks

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a> function to allocate the memory for the object.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemrealloc">SnmpUtilMemReAlloc</a>