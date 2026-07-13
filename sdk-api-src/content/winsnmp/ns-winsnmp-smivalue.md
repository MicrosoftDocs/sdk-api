---
UID: NS:winsnmp.smiVALUE
title: smiVALUE (winsnmp.h)
description: The WinSNMP smiVALUE structure describes the value associated with a variable name in a variable binding entry.
helpviewer_keywords: ["*smiLPVALUE","SNMP_SYNTAX_CNTR32","SNMP_SYNTAX_CNTR64","SNMP_SYNTAX_ENDOFMIBVIEW","SNMP_SYNTAX_GAUGE32","SNMP_SYNTAX_INT","SNMP_SYNTAX_INT32","SNMP_SYNTAX_IPADDR","SNMP_SYNTAX_NOSUCHINSTANCE","SNMP_SYNTAX_NOSUCHOBJECT","SNMP_SYNTAX_NULL","SNMP_SYNTAX_OCTETS","SNMP_SYNTAX_OID","SNMP_SYNTAX_OPAQUE","SNMP_SYNTAX_TIMETICKS","SNMP_SYNTAX_UINT32","_snmp_smivalue_str","smiLPVALUE","smiLPVALUE structure pointer [SNMP]","smiVALUE","smiVALUE structure [SNMP]","snmp.smivalue_str","winsnmp/smiLPVALUE","winsnmp/smiVALUE"]
old-location: snmp\smivalue_str.htm
tech.root: SNMP
ms.assetid: e5e8f321-54b2-469d-bdd3-9867fd85b447
ms.date: 12/05/2018
ms.keywords: '*smiLPVALUE, SNMP_SYNTAX_CNTR32, SNMP_SYNTAX_CNTR64, SNMP_SYNTAX_ENDOFMIBVIEW, SNMP_SYNTAX_GAUGE32, SNMP_SYNTAX_INT, SNMP_SYNTAX_INT32, SNMP_SYNTAX_IPADDR, SNMP_SYNTAX_NOSUCHINSTANCE, SNMP_SYNTAX_NOSUCHOBJECT, SNMP_SYNTAX_NULL, SNMP_SYNTAX_OCTETS, SNMP_SYNTAX_OID, SNMP_SYNTAX_OPAQUE, SNMP_SYNTAX_TIMETICKS, SNMP_SYNTAX_UINT32, _snmp_smivalue_str, smiLPVALUE, smiLPVALUE structure pointer [SNMP], smiVALUE, smiVALUE structure [SNMP], snmp.smivalue_str, winsnmp/smiLPVALUE, winsnmp/smiVALUE'
req.header: winsnmp.h
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
req.typenames: smiVALUE, *smiLPVALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - smiLPVALUE
 - winsnmp/smiLPVALUE
 - smiVALUE
 - winsnmp/smiVALUE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsnmp.h
api_name:
 - smiVALUE
---

# smiVALUE structure


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>smiVALUE</b> structure describes the value associated with a variable name in a variable binding entry.

The <b>syntax</b> member of the 
<b>smiVALUE</b> structure contains a WinSNMP data type that indicates the type of data in the <b>value</b> member. The <b>value</b> member of the structure is the union of all possible WinSNMP data types.

## -struct-fields

### -field syntax

Type: <b>smiUINT32</b>

Specifies an unsigned long integer that indicates the syntax data type of the <b>value</b> member. This member can be only one of the types listed in the following table. For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-types">WinSNMP Data Types</a> and RFC 1902, "Structure of Management Information for Version 2 of the Simple Network Management Protocol (SNMPv2)."

<table>
<tr>
<th>Syntax data type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_INT"></a><a id="snmp_syntax_int"></a><dl>
<dt><b>SNMP_SYNTAX_INT</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit signed integer variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_OCTETS"></a><a id="snmp_syntax_octets"></a><dl>
<dt><b>SNMP_SYNTAX_OCTETS</b></dt>
</dl>
</td>
<td width="60%">
Indicates an octet string variable that is binary or textual data.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_NULL"></a><a id="snmp_syntax_null"></a><dl>
<dt><b>SNMP_SYNTAX_NULL</b></dt>
</dl>
</td>
<td width="60%">
Indicates a <b>NULL</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_OID"></a><a id="snmp_syntax_oid"></a><dl>
<dt><b>SNMP_SYNTAX_OID</b></dt>
</dl>
</td>
<td width="60%">
Indicates an object identifier variable that is an assigned name with a maximum of 128 subidentifiers.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_INT32"></a><a id="snmp_syntax_int32"></a><dl>
<dt><b>SNMP_SYNTAX_INT32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit signed integer variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_IPADDR"></a><a id="snmp_syntax_ipaddr"></a><dl>
<dt><b>SNMP_SYNTAX_IPADDR</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit Internet address variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_CNTR32"></a><a id="snmp_syntax_cntr32"></a><dl>
<dt><b>SNMP_SYNTAX_CNTR32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a counter variable that increases until it reaches a maximum value of (2^32) – 1.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_GAUGE32"></a><a id="snmp_syntax_gauge32"></a><dl>
<dt><b>SNMP_SYNTAX_GAUGE32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a gauge variable that is a non-negative integer that can increase or decrease, but never exceed a maximum value.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_TIMETICKS"></a><a id="snmp_syntax_timeticks"></a><dl>
<dt><b>SNMP_SYNTAX_TIMETICKS</b></dt>
</dl>
</td>
<td width="60%">
Indicates a counter variable that measures the time in hundredths of a second, until it reaches a maximum value of (2^32) – 1. It is a non-negative integer that is relative to a specific timer event.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_OPAQUE"></a><a id="snmp_syntax_opaque"></a><dl>
<dt><b>SNMP_SYNTAX_OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
This type provides backward compatibility, and should not be used for new object types. It supports the capability to pass arbitrary Abstract Syntax Notation One (ASN.1) syntax.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_CNTR64"></a><a id="snmp_syntax_cntr64"></a><dl>
<dt><b>SNMP_SYNTAX_CNTR64</b></dt>
</dl>
</td>
<td width="60%">
Indicates a counter variable that increases until it reaches a maximum value of (2^64) – 1.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_UINT32"></a><a id="snmp_syntax_uint32"></a><dl>
<dt><b>SNMP_SYNTAX_UINT32</b></dt>
</dl>
</td>
<td width="60%">
Indicates a 32-bit unsigned integer variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_NOSUCHOBJECT"></a><a id="snmp_syntax_nosuchobject"></a><dl>
<dt><b>SNMP_SYNTAX_NOSUCHOBJECT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the agent does not support the object type that corresponds to the variable.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_NOSUCHINSTANCE"></a><a id="snmp_syntax_nosuchinstance"></a><dl>
<dt><b>SNMP_SYNTAX_NOSUCHINSTANCE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the object instance does not exist for the operation.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_SYNTAX_ENDOFMIBVIEW"></a><a id="snmp_syntax_endofmibview"></a><dl>
<dt><b>SNMP_SYNTAX_ENDOFMIBVIEW</b></dt>
</dl>
</td>
<td width="60%">
Indicates the WinSNMP application is attempting to reference an object identifier that is beyond the end of the MIB tree that the agent supports.

</td>
</tr>
</table>
 

The last three syntax types describe exception conditions under the SNMP version 2C (SNMPv2C) framework.

### -field value

Specifies the union of all possible WinSNMP syntax data types, including the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> or 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> descriptor types.



#### sNumber

Type: <b>smiINT</b>

Specifies a signed long integer value.



#### uNumber

Type: <b>smiUINT32</b>

Specifies a 32-bit unsigned long integer value.



#### hNumber

Type: <b>smiCNTR64</b>

Specifies a 64-bit unsigned integer value



#### string

Type: <b>smiOCTETS</b>

Specifies a string.



#### oid

Type: <b>smiOID</b>

Specifies an object identifier (OID).



#### empty

Type: <b>smiBYTE</b>

Specifies an empty member.

### -field sNumber

### -field uNumber

### -field hNumber

### -field string

### -field oid

### -field empty

## -remarks

A WinSNMP application must check the <b>syntax</b> member of an 
<b>smiVALUE</b> structure to correctly dereference the <b>value</b> member. The <b>value</b> member can contain a simple scalar value or a non-scalar value like an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> or an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> descriptor structure.

If the <b>syntax</b> member indicates that the <b>value</b> member is an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> or an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> descriptor structure, the WinSNMP application must determine whether to free the resources allocated for the structure. The Microsoft WinSNMP implementation allocates and deallocates memory for all output 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> and 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structures. The application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free the memory for the <b>ptr</b> member of these structures.

Because the WinSNMP application allocates memory for input descriptors with variable lengths, it must free that memory. For more information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/SNMP/winsnmp-structures">WinSNMP Structures</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>

