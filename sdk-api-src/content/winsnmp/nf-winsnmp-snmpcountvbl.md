---
UID: NF:winsnmp.SnmpCountVbl
title: SnmpCountVbl function (winsnmp.h)
description: A WinSNMP application calls the WinSNMP SnmpCountVbl function to enumerate the variable binding entries in the specified variable bindings list.
helpviewer_keywords: ["SnmpCountVbl","SnmpCountVbl function [SNMP]","_snmp_snmpcountvbl","snmp.snmpcountvbl","winsnmp/SnmpCountVbl"]
old-location: snmp\snmpcountvbl.htm
tech.root: SNMP
ms.assetid: 08e7d450-0c75-4ef5-a9c5-ef0255601a9a
ms.date: 12/05/2018
ms.keywords: SnmpCountVbl, SnmpCountVbl function [SNMP], _snmp_snmpcountvbl, snmp.snmpcountvbl, winsnmp/SnmpCountVbl
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
 - SnmpCountVbl
 - winsnmp/SnmpCountVbl
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
 - SnmpCountVbl
---

# SnmpCountVbl function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the WinSNMP 
<b>SnmpCountVbl</b> function to enumerate the variable binding entries in the specified variable bindings list.

## -parameters

### -param vbl [in]

Handle to the variable bindings list to enumerate.

## -returns

If the function succeeds, the return value is the count of variable binding entries in the variable bindings list.

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
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The variable bindings list does not contain any variable binding entries at this time.

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

The 
<b>SnmpCountVbl</b> function returns an unsigned integer value that is the maximum value the WinSNMP application can specify for the <i>index</i> parameter in the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetvb">SnmpSetVb</a>, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdeletevb">SnmpDeleteVb</a> functions.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpdeletevb">SnmpDeleteVb</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetvb">SnmpGetVb</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsetvb">SnmpSetVb</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>