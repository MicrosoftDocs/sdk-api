---
UID: NF:snmp.SnmpUtilMemAlloc
title: SnmpUtilMemAlloc function (snmp.h)
description: The SnmpUtilMemAlloc function allocates dynamic memory from the process heap. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilMemAlloc","SnmpUtilMemAlloc function [SNMP]","_snmp_snmputilmemalloc","snmp.snmputilmemalloc","snmp/SnmpUtilMemAlloc"]
old-location: snmp\snmputilmemalloc.htm
tech.root: SNMP
ms.assetid: 85e293da-4c5b-4b32-9b86-e63074d37274
ms.date: 12/05/2018
ms.keywords: SnmpUtilMemAlloc, SnmpUtilMemAlloc function [SNMP], _snmp_snmputilmemalloc, snmp.snmputilmemalloc, snmp/SnmpUtilMemAlloc
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
 - SnmpUtilMemAlloc
 - snmp/SnmpUtilMemAlloc
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
 - SnmpUtilMemAlloc
---

# SnmpUtilMemAlloc function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilMemAlloc</b> function allocates dynamic memory from the process heap. This function is an element of the SNMP Utility API.

## -parameters

### -param nBytes [in]

Specifies the number of bytes to allocate for the memory object.

## -returns

If the function succeeds, the return value is a pointer to the newly allocated memory object.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Use the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a> function to release memory that the 
<b>SnmpUtilMemAlloc</b> function allocates.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemrealloc">SnmpUtilMemReAlloc</a>