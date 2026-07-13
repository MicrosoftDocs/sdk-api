---
UID: NS:snmp.AsnOctetString
title: AsnOctetString (snmp.h)
description: The AsnOctetString structure contains octet quantities, usually bytes. This structure is used by multiple SNMP functions. This structure is not used by the WinSNMP API functions.
helpviewer_keywords: ["AsnBits","AsnDisplayString","AsnIPAddress","AsnImplicitSequence","AsnNetworkAddress","AsnOctetString","AsnOctetString structure [SNMP]","AsnOpaque","AsnSequence","_snmp_asnoctetstring_str","snmp.asnoctetstring_str","snmp/AsnOctetString"]
old-location: snmp\asnoctetstring_str.htm
tech.root: SNMP
ms.assetid: d58c54e2-0479-408f-977d-63409e5f500e
ms.date: 12/05/2018
ms.keywords: AsnBits, AsnDisplayString, AsnIPAddress, AsnImplicitSequence, AsnNetworkAddress, AsnOctetString, AsnOctetString structure [SNMP], AsnOpaque, AsnSequence, _snmp_asnoctetstring_str, snmp.asnoctetstring_str, snmp/AsnOctetString
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AsnOctetString
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AsnOctetString
 - snmp/AsnOctetString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Snmp.h
api_name:
 - AsnOctetString
---

# AsnOctetString structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>AsnOctetString</b> structure contains octet quantities, usually bytes. This structure is used by multiple SNMP functions. This structure is not used by the 
<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API</a> functions.

## -struct-fields

### -field stream

Pointer to the octet stream.

### -field length

The number of octets in the data stream.

### -field dynamic

Flag that specifies whether the data stream has been dynamically allocated with the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a> function.

## -remarks

Use the 
<b>AsnOctetString</b> structure to transfer string values. For example, use it to transfer the string that represents a computer name as a MIB object value.

You must check the flag specified in the <b>dynamic</b> member before you release the data stream of an octet string. Call the 
<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a> function only if the <b>dynamic</b> member is set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/SNMP/snmp-structures">SNMP Structures</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemalloc">SnmpUtilMemAlloc</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmputilmemfree">SnmpUtilMemFree</a>

