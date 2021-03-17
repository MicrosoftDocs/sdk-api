---
UID: NF:winsnmp.SnmpSetVb
title: SnmpSetVb function (winsnmp.h)
description: The WinSNMP SnmpSetVb function changes variable binding entries in a variable bindings list. This function also appends new variable binding entries to an existing variable bindings list.
helpviewer_keywords: ["SnmpSetVb","SnmpSetVb function [SNMP]","_snmp_snmpsetvb","snmp.snmpsetvb","winsnmp/SnmpSetVb"]
old-location: snmp\snmpsetvb.htm
tech.root: SNMP
ms.assetid: 65d962bd-f4d7-4cf4-9b24-a7678e669e24
ms.date: 12/05/2018
ms.keywords: SnmpSetVb, SnmpSetVb function [SNMP], _snmp_snmpsetvb, snmp.snmpsetvb, winsnmp/SnmpSetVb
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
 - SnmpSetVb
 - winsnmp/SnmpSetVb
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
 - SnmpSetVb
---

# SnmpSetVb function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetVb</b> function changes variable binding entries in a variable bindings list. This function also appends new variable binding entries to an existing variable bindings list.

## -parameters

### -param vbl [in]

Handle to the variable bindings list to update.

### -param index [in]

Specifies an unsigned long integer variable that contains the position of the variable binding entry, within the variable bindings list, if this is an update operation. If this is an append operation, this parameter must be equal to zero. For more information, see the following Remarks section.

### -param name [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure that represents the name of the variable to append or change. For more information, see the following Remarks section.

### -param value [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure. The structure contains the value associated with the variable specified by the <i>name</i> parameter.

## -returns

If the function succeeds, the return value is the position of the updated or appended variable binding entry in the variable bindings list. For additional information, see the following Remarks section.

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
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_SYNTAX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>syntax</b> member of the structure pointed to by the <i>value</i> parameter is invalid.

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

Valid values for the <i>index</i> parameter range from zero to n. The value zero indicates an append operation. The value n is the total number of variable binding entries in the variable bindings list. A WinSNMP application should call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a> function before it calls 
<b>SnmpSetVb</b> to obtain the total number of variable binding entries.

If the function successfully performs an update operation, the return value equals the value of the <i>index</i> parameter. If the function appends a variable binding entry, the return value is n + 1.

If the <i>name</i> parameter is not <b>NULL</b>, but the <i>value</i> parameter is <b>NULL</b>, the Microsoft WinSNMP implementation initializes the new variable binding entry with the <b>value</b> member set to <b>NULL</b> and with the <b>syntax</b> member set to <a href="/windows/desktop/SNMP/snmp-variable-types-and-request-pdu-types">SNMP_SYNTAX_</a>.

If the <i>index</i> parameter is not equal to zero, and the <i>name</i> parameter is <b>NULL</b>, the Microsoft WinSNMP implementation updates only the value of the variable pointed to by the <i>index</i> parameter.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcountvbl">SnmpCountVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>