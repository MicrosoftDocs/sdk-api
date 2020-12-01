---
UID: NF:winsnmp.SnmpStrToOid
title: SnmpStrToOid function (winsnmp.h)
description: The WinSNMP SnmpStrToOid function converts the dotted numeric string format of an SNMP object identifier, for example, &quot;1.2.3.4.5.6&quot;, to its internal binary representation.
helpviewer_keywords: ["SnmpStrToOid","SnmpStrToOid function [SNMP]","_snmp_snmpstrtooid","snmp.snmpstrtooid","winsnmp/SnmpStrToOid"]
old-location: snmp\snmpstrtooid.htm
tech.root: SNMP
ms.assetid: cbcf8fc6-c5d6-476b-9490-4b87fd6a8a56
ms.date: 12/05/2018
ms.keywords: SnmpStrToOid, SnmpStrToOid function [SNMP], _snmp_snmpstrtooid, snmp.snmpstrtooid, winsnmp/SnmpStrToOid
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
 - SnmpStrToOid
 - winsnmp/SnmpStrToOid
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
 - SnmpStrToOid
---

# SnmpStrToOid function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpStrToOid</b> function converts the dotted numeric string format of an SNMP object identifier, for example, "1.2.3.4.5.6", to its internal binary representation.

## -parameters

### -param string [in]

Pointer to a <b>null</b>-terminated object identifier string to convert.

### -param dstOID [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure that receives the converted value.

## -returns

If the function succeeds, the return value is the number of subidentifiers in the converted object identifier. This number is also the value of the <b>len</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure pointed to by the <i>dstOID</i> parameter.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>string</i> parameter is invalid. For additional information, see the following Remarks section.

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

The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to free resources allocated for the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure pointed to by the <i>dstOID</i> parameter. On input, 
<b>SnmpFreeDescriptor</b> ignores the members of this 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure. The Microsoft WinSNMP implementation overwrites the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> members if the function completes successfully.

The 
<b>SnmpStrToOid</b> function fails and returns the SNMPAPI_OID_INVALID error code if the <i>string</i> parameter meets one of the following conditions:

<ul>
<li>Is not <b>null</b>-terminated.</li>
<li>Is not the textual form of a valid object identifier.</li>
<li>Is insufficient in length; all object identifiers must have two subidentifiers.</li>
<li>Exceeds the MAXOBJIDSTRSIZE of 1408 bytes.</li>
</ul>
For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a> and 
<a href="/windows/desktop/SNMP/freeing-winsnmp-descriptors">Freeing WinSNMP Descriptors</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>