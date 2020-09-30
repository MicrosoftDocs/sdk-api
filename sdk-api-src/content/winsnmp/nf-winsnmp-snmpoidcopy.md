---
UID: NF:winsnmp.SnmpOidCopy
title: SnmpOidCopy function (winsnmp.h)
description: The WinSNMP SnmpOidCopy function copies an SNMP object identifier, allocating any necessary memory for the copy.
helpviewer_keywords: ["SnmpOidCopy","SnmpOidCopy function [SNMP]","_snmp_snmpoidcopy","snmp.snmpoidcopy","winsnmp/SnmpOidCopy"]
old-location: snmp\snmpoidcopy.htm
tech.root: SNMP
ms.assetid: ab121160-1c4f-41c0-a738-2e7605780ed2
ms.date: 12/05/2018
ms.keywords: SnmpOidCopy, SnmpOidCopy function [SNMP], _snmp_snmpoidcopy, snmp.snmpoidcopy, winsnmp/SnmpOidCopy
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
 - SnmpOidCopy
 - winsnmp/SnmpOidCopy
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
 - SnmpOidCopy
---

# SnmpOidCopy function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpOidCopy</b> function copies an SNMP object identifier, allocating any necessary memory for the copy.

## -parameters

### -param srcOID [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure to copy.

### -param dstOID [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure to receive a copy of the object identifier specified by the <i>srcOID</i> parameter.

## -returns

If the function succeeds, the return value is the number of subidentifiers in the copied object identifier. This number is also the value of the <b>len</b> member of the 
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
The <i>srcOID</i> parameter is invalid.

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

On input, the 
<b>SnmpOidCopy</b> function ignores the members of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure pointed to by the <i>dstOID</i> parameter. The Microsoft WinSNMP implementation overwrites the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> members if the function completes successfully.

The WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a> function to enable the implementation to free resources allocated for the <b>ptr</b> member of the 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure pointed to by the <i>dstOID</i> parameter. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a> and 
<a href="/windows/desktop/SNMP/freeing-winsnmp-descriptors">Freeing WinSNMP Descriptors</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreedescriptor">SnmpFreeDescriptor</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>