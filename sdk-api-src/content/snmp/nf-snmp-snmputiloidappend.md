---
UID: NF:snmp.SnmpUtilOidAppend
title: SnmpUtilOidAppend function (snmp.h)
description: The SnmpUtilOidAppend function appends the source object identifier to the destination object identifier. This function is an element of the SNMP Utility API.
helpviewer_keywords: ["SnmpUtilOidAppend","SnmpUtilOidAppend function [SNMP]","_snmp_snmputiloidappend","snmp.snmputiloidappend","snmp/SnmpUtilOidAppend"]
old-location: snmp\snmputiloidappend.htm
tech.root: SNMP
ms.assetid: 8ffa5638-13ef-4cec-80f0-303611a52dac
ms.date: 12/05/2018
ms.keywords: SnmpUtilOidAppend, SnmpUtilOidAppend function [SNMP], _snmp_snmputiloidappend, snmp.snmputiloidappend, snmp/SnmpUtilOidAppend
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
 - SnmpUtilOidAppend
 - snmp/SnmpUtilOidAppend
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
 - SnmpUtilOidAppend
---

# SnmpUtilOidAppend function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpUtilOidAppend</b> function appends the source object identifier to the destination object identifier. This function is an element of the SNMP Utility API.

## -parameters

### -param pOidDst [in, out]

Pointer to an 
<a href="/windows/desktop/api/snmp/ns-snmp-asnobjectidentifier">AsnObjectIdentifier</a> structure to receive the source structure.

### -param pOidSrc [in]

Pointer to an 
<b>AsnObjectIdentifier</b> structure to append.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. This function does not generate Windows Sockets errors. The application should call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. <b>GetLastError</b> may return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_BERAPI_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Indicates an overflow condition

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMP_MEM_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Indicates a memory allocation error

</td>
</tr>
</table>

## -remarks

The 
<b>SnmpUtilOidAppend</b> function calls the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemrealloc">SnmpUtilMemReAlloc</a> function. The 
<b>SnmpUtilMemReAlloc</b> function expands the buffer for the destination object identifier.

Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a> function to free memory that the 
<b>SnmpUtilOidAppend</b> function allocates for the destination.

## -see-also

<a href="/windows/desktop/SNMP/snmp-functions">SNMP Functions</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemrealloc">SnmpUtilMemReAlloc</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputiloidfree">SnmpUtilOidFree</a>