---
UID: NF:winsnmp.SnmpGetVb
title: SnmpGetVb function (winsnmp.h)
description: A WinSNMP application calls the SnmpGetVb function to retrieve information from a variable bindings list. This WinSNMP function retrieves a variable name and its associated value from the variable binding entry specified by the index parameter.
helpviewer_keywords: ["SNMP_SYNTAX_CNTR32","SNMP_SYNTAX_CNTR64","SNMP_SYNTAX_ENDOFMIBVIEW","SNMP_SYNTAX_GAUGE32","SNMP_SYNTAX_INT","SNMP_SYNTAX_INT32","SNMP_SYNTAX_IPADDR","SNMP_SYNTAX_NOSUCHINSTANCE","SNMP_SYNTAX_NOSUCHOBJECT","SNMP_SYNTAX_NULL","SNMP_SYNTAX_OCTETS","SNMP_SYNTAX_OID","SNMP_SYNTAX_OPAQUE","SNMP_SYNTAX_TIMETICKS","SNMP_SYNTAX_UINT32","SnmpGetVb","SnmpGetVb function [SNMP]","_snmp_snmpgetvb","snmp.snmpgetvb","winsnmp/SnmpGetVb"]
old-location: snmp\snmpgetvb.htm
tech.root: SNMP
ms.assetid: a6598b4e-6797-4e18-8ab5-059c75bc84ef
ms.date: 12/05/2018
ms.keywords: SNMP_SYNTAX_CNTR32, SNMP_SYNTAX_CNTR64, SNMP_SYNTAX_ENDOFMIBVIEW, SNMP_SYNTAX_GAUGE32, SNMP_SYNTAX_INT, SNMP_SYNTAX_INT32, SNMP_SYNTAX_IPADDR, SNMP_SYNTAX_NOSUCHINSTANCE, SNMP_SYNTAX_NOSUCHOBJECT, SNMP_SYNTAX_NULL, SNMP_SYNTAX_OCTETS, SNMP_SYNTAX_OID, SNMP_SYNTAX_OPAQUE, SNMP_SYNTAX_TIMETICKS, SNMP_SYNTAX_UINT32, SnmpGetVb, SnmpGetVb function [SNMP], _snmp_snmpgetvb, snmp.snmpgetvb, winsnmp/SnmpGetVb
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
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpGetVb
 - winsnmp/SnmpGetVb
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpGetVb
---

# SnmpGetVb function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpGetVb</b> function to retrieve information from a variable bindings list. This WinSNMP function retrieves a variable name and its associated value from the variable binding entry specified by the <i>index</i> parameter.

## -parameters

### -param vbl [in]

Handle to the variable bindings list to retrieve.

### -param index [in]

Specifies an unsigned long integer variable that identifies the variable binding entry to retrieve. This variable contains the position of the variable binding entry, within the variable bindings list. 




Valid values for this parameter are in the range from 1 to n, where 1 indicates the first variable binding entry in the variable bindings list, and n is the total number of entries in the list. For additional information, see the following Remarks section.

### -param name [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure to receive the variable name of the variable binding entry.

### -param value [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure to receive the value associated with the variable identified by the <i>name</i> parameter. 




If the function succeeds, the <b>syntax</b> member of the structure pointed to by the <i>value</i> parameter can be one of the following syntax data types. For additional information, see RFC 1902, "Structure of Management Information for Version 2 of the Simple Network Management Protocol (SNMPv2)."

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
Indicates a 32-bit Internet address variable. If SNMPv1 PDU trap format is used to represent an IPv6 address, this value is 0.0.0.0.

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

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ALLOC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_INDEX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_VBL_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>vbl</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown or undefined error occurred.

</td>
</tr>
</table>

## -remarks

The last three syntax types describe exception conditions under the SNMP version 2C(SNMPv2C) framework.

The 
<b>SnmpGetVb</b> function returns the variable name of the variable binding entry in the structure pointed to by the <i>name</i> parameter. It returns the variable's associated value in the structure pointed to by the <i>value</i> parameter.

On input, the 
<b>SnmpGetVb</b> function ignores the members of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> and 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structures pointed to by the <i>name</i> and <i>value</i> parameters respectively. The Microsoft WinSNMP implementation overwrites the members if the function completes successfully.

Valid values for a WinSNMP application to use for the <i>index</i> parameter are as follows:

<ul>
<li>The return value from a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a> function</li>
<li>The error index field of an <b>SNMP_PDU_RESPONSE</b> protocol data unit (PDU) returned by a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a> function</li>
</ul>
The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free resources allocated for the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure pointed to by the <i>name</i> parameter. The application must also call the 
<b>SnmpFreeDescriptor</b> function to release resources allocated for the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure pointed to by the <i>value</i> parameter under the conditions following. If the <b>value</b> member is an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a> or an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure, the application must call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> to free the resources allocated for these structures. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmprecvmsg">SnmpRecvMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioctets">smiOCTETS</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>