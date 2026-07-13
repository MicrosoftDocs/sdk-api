---
UID: NS:snmp.AsnAny
title: AsnAny (snmp.h)
description: The AsnAny structure contains an SNMP variable type and value. This structure is a member of the SnmpVarBind structure that is used as a parameter in many of the SNMP functions. This structure is not used by the WinSNMP API functions.
helpviewer_keywords: ["ASN_BITS","ASN_COUNTER32","ASN_COUNTER64","ASN_GAUGE32","ASN_INTEGER","ASN_INTEGER32","ASN_IPADDRESS","ASN_OBJECTIDENTIFIER","ASN_OCTETSTRING","ASN_OPAQUE","ASN_SEQUENCE","ASN_TIMETICKS","ASN_UNSIGNED32","AsnAny","AsnAny structure [SNMP]","AsnObjectSyntax","SNMP_EXCEPTION_ENDOFMIBVIEW","SNMP_EXCEPTION_NOSUCHINSTANCE","SNMP_EXCEPTION_NOSUCHOBJECT","_snmp_asnany_str","snmp.asnany_str","snmp/AsnAny"]
old-location: snmp\asnany_str.htm
tech.root: SNMP
ms.assetid: ce8d002e-f357-499c-b976-f8ebaf1e7142
ms.date: 12/05/2018
ms.keywords: ASN_BITS, ASN_COUNTER32, ASN_COUNTER64, ASN_GAUGE32, ASN_INTEGER, ASN_INTEGER32, ASN_IPADDRESS, ASN_OBJECTIDENTIFIER, ASN_OCTETSTRING, ASN_OPAQUE, ASN_SEQUENCE, ASN_TIMETICKS, ASN_UNSIGNED32, AsnAny, AsnAny structure [SNMP], AsnObjectSyntax, SNMP_EXCEPTION_ENDOFMIBVIEW, SNMP_EXCEPTION_NOSUCHINSTANCE, SNMP_EXCEPTION_NOSUCHOBJECT, _snmp_asnany_str, snmp.asnany_str, snmp/AsnAny
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
req.typenames: AsnAny
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AsnAny
 - snmp/AsnAny
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
 - AsnAny
---

# AsnAny structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>AsnAny</b> structure contains an SNMP variable type and value. This structure is a member of the 
<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a> structure that is used as a parameter in many of the SNMP functions. This structure is not used by the 
<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API</a> functions.

## -struct-fields

### -field asnType

Type: <b>BYTE</b>

Indicates the variable's type. This member must be only one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ASN_INTEGER"></a><a id="asn_integer"></a><dl>
<dt><b>ASN_INTEGER</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit signed integer variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_INTEGER32"></a><a id="asn_integer32"></a><dl>
<dt><b>ASN_INTEGER32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit signed integer variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_UNSIGNED32"></a><a id="asn_unsigned32"></a><dl>
<dt><b>ASN_UNSIGNED32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit unsigned integer variable. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_COUNTER64"></a><a id="asn_counter64"></a><dl>
<dt><b>ASN_COUNTER64</b></dt>
</dl>
</td>
<td width="60%">
Indicates a counter variable that increases until it reaches a maximum value of (2^64) – 1.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_OCTETSTRING"></a><a id="asn_octetstring"></a><dl>
<dt><b>ASN_OCTETSTRING</b></dt>
</dl>
</td>
<td width="60%">
Indicates an octet string variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_BITS"></a><a id="asn_bits"></a><dl>
<dt><b>ASN_BITS</b></dt>
</dl>
</td>
<td width="60%">
Indicates a variable that is an enumeration of named bits.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_OBJECTIDENTIFIER"></a><a id="asn_objectidentifier"></a><dl>
<dt><b>ASN_OBJECTIDENTIFIER</b></dt>
</dl>
</td>
<td width="60%">
Indicates an object identifier variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_SEQUENCE"></a><a id="asn_sequence"></a><dl>
<dt><b>ASN_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an ASN sequence variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_IPADDRESS"></a><a id="asn_ipaddress"></a><dl>
<dt><b>ASN_IPADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Indicates an IP address variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_COUNTER32"></a><a id="asn_counter32"></a><dl>
<dt><b>ASN_COUNTER32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a counter variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_GAUGE32"></a><a id="asn_gauge32"></a><dl>
<dt><b>ASN_GAUGE32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a gauge variable. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_TIMETICKS"></a><a id="asn_timeticks"></a><dl>
<dt><b>ASN_TIMETICKS</b></dt>
</dl>
</td>
<td width="60%">
Indicates a timeticks variable.

</td>
</tr>
<tr>
<td width="40%"><a id="ASN_OPAQUE"></a><a id="asn_opaque"></a><dl>
<dt><b>ASN_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an opaque variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXCEPTION_NOSUCHOBJECT"></a><a id="snmp_exception_nosuchobject"></a><dl>
<dt><b>SNMP_EXCEPTION_NOSUCHOBJECT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the object provided is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXCEPTION_NOSUCHINSTANCE"></a><a id="snmp_exception_nosuchinstance"></a><dl>
<dt><b>SNMP_EXCEPTION_NOSUCHINSTANCE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the instance provided is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_EXCEPTION_ENDOFMIBVIEW"></a><a id="snmp_exception_endofmibview"></a><dl>
<dt><b>SNMP_EXCEPTION_ENDOFMIBVIEW</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the end of the MIB view has been reached.

</td>
</tr>
</table>

### -field asnValue

Contains the variable's value. This member can be only one of the following values.



#### number

Type: <b>AsnInteger32</b>

Accesses a 32-bit signed integer variable.



#### unsigned32

Type: <b>AsnUnsigned32</b>

Accesses a 32-bit unsigned integer variable.



#### counter64

Type: <b>AsnCounter64</b>

Accesses a counter variable that increases until it reaches a maximum value of (2^64) – 1.



#### string

Type: <b>AsnOctetString</b>

Accesses an octet string variable.



#### bits

Type: <b>AsnBits</b>

Accesses a variable that is an enumeration of named bits with non-negative, contiguous values, starting at zero.



#### object

Type: <b>AsnObjectIdentifier</b>

Accesses an object identifier variable.



#### sequence

Type: <b>AsnSequence</b>

Accesses an ASN sequence variable.



#### address

Type: <b>AsnIPAddress</b>

Accesses an IP address variable.



#### counter

Type: <b>AsnCounter32</b>

Accesses a counter variable that increases until it reaches a maximum value of (2^32) – 1.



#### gauge

Type: <b>AsnGauge32</b>

Accesses a gauge variable.



#### ticks

Type: <b>AsnTimeticks</b>

Accesses a timeticks counter variable that is relative to a specific timer event.



#### arbitrary

Type: <b>AsnOpaque</b>

Accesses an opaque variable.

### -field number

### -field unsigned32

### -field counter64

### -field string

### -field bits

### -field object

### -field sequence

### -field address

### -field counter

### -field gauge

### -field ticks

### -field arbitrary

## -remarks

To use the definition of the Unsigned32 type described in RFC 1902, you can specify the ASN_GAUGE32 variable type. Currently the ASN_UNSIGNED32 variable type specifies the UInteger32 type described in RFC 1442.

## -see-also

<a href="/windows/desktop/SNMP/snmp-structures">SNMP Structures</a>



<a href="/windows/desktop/SNMP/simple-network-management-protocol-snmp-">Simple Network Management Protocol (SNMP) Overview</a>



<a href="/windows/desktop/api/snmp/nf-snmp-snmpextensionmonitor">SnmpExtensionMonitor</a>



<a href="/windows/desktop/api/snmp/ns-snmp-snmpvarbind">SnmpVarBind</a>

