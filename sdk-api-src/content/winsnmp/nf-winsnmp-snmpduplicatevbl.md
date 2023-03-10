---
UID: NF:winsnmp.SnmpDuplicateVbl
title: SnmpDuplicateVbl function (winsnmp.h)
description: The WinSNMP SnmpDuplicateVbl function copies a variable bindings list for the specified WinSNMP session. This function returns a handle to the copied variable bindings list and allocates any necessary memory for it.
helpviewer_keywords: ["SnmpDuplicateVbl","SnmpDuplicateVbl function [SNMP]","_snmp_snmpduplicatevbl","snmp.snmpduplicatevbl","winsnmp/SnmpDuplicateVbl"]
old-location: snmp\snmpduplicatevbl.htm
tech.root: SNMP
ms.assetid: b6ca0167-43d7-4a85-b3ba-c2683ae27ff5
ms.date: 12/05/2018
ms.keywords: SnmpDuplicateVbl, SnmpDuplicateVbl function [SNMP], _snmp_snmpduplicatevbl, snmp.snmpduplicatevbl, winsnmp/SnmpDuplicateVbl
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
 - SnmpDuplicateVbl
 - winsnmp/SnmpDuplicateVbl
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
 - SnmpDuplicateVbl
---

# SnmpDuplicateVbl function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDuplicateVbl</b> function copies a variable bindings list for the specified WinSNMP session. This function returns a handle to the copied variable bindings list and allocates any necessary memory for it.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param vbl [in]

Handle to the variable bindings list to copy. The source variable bindings list can be empty.

## -returns

If the function succeeds, the return value is a handle to a new variable bindings list.

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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The session handle is invalid.

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
<b>SnmpDuplicateVbl</b> function creates a new variable bindings list for the specified WinSNMP session. This function initializes the new list with a copy of the data in the source variable bindings list.

The handle the 
<b>SnmpDuplicateVbl</b> function returns is unique among the variable bindings list handles that are active within the WinSNMP application.

The WinSNMP application must release the resources associated with each variable bindings list. It should do this by matching each call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a> and 
<b>SnmpDuplicateVbl</b> functions with a corresponding call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<b>SnmpCreateVbl</b> or 
<b>SnmpDuplicateVbl</b>. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>