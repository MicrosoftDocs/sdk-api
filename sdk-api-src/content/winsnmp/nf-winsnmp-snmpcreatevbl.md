---
UID: NF:winsnmp.SnmpCreateVbl
title: SnmpCreateVbl function (winsnmp.h)
description: The WinSNMP SnmpCreateVbl function creates a new variable bindings list for the calling WinSNMP application.
helpviewer_keywords: ["SnmpCreateVbl","SnmpCreateVbl function [SNMP]","_snmp_snmpcreatevbl","snmp.snmpcreatevbl","winsnmp/SnmpCreateVbl"]
old-location: snmp\snmpcreatevbl.htm
tech.root: SNMP
ms.assetid: 5e973b32-3e7e-41f7-9257-4ac3d67fd853
ms.date: 12/05/2018
ms.keywords: SnmpCreateVbl, SnmpCreateVbl function [SNMP], _snmp_snmpcreatevbl, snmp.snmpcreatevbl, winsnmp/SnmpCreateVbl
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
 - SnmpCreateVbl
 - winsnmp/SnmpCreateVbl
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
 - SnmpCreateVbl
---

# SnmpCreateVbl function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpCreateVbl</b> function creates a new variable bindings list for the calling WinSNMP application. If the <i>name</i> and <i>value</i> parameters are not <b>NULL</b>, 
<b>SnmpCreateVbl</b> uses their values to create the first variable binding entry for the new variable bindings list. The 
<b>SnmpCreateVbl</b> function returns a handle to the new variable bindings list and allocates any necessary memory for it.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param name [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure that contains the variable name for the first variable binding entry. This parameter can be <b>NULL</b>. For additional information, see the following Remarks section.

### -param value [in]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a> structure that contains a value to associate with the variable in the first variable binding entry. This parameter can be <b>NULL</b>. For additional information, see the following Remarks section.

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
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter references an invalid 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a> structure.

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

The 
<b>SnmpCreateVbl</b> function uses the values of the <i>name</i> and <i>value</i> parameters to create and initialize the first variable binding entry of a new variable bindings list. If the <i>name</i> parameter is <b>NULL</b>, the Microsoft WinSNMP implementation ignores the <i>value</i> parameter and creates an empty variable bindings list.

If the <i>name</i> parameter is not <b>NULL</b>, but the <i>value</i> parameter is <b>NULL</b>, the implementation creates and initializes the first variable binding entry in the variable bindings list. It initializes the <b>syntax</b> member of the structure pointed to by the <i>value</i> parameter with the value SNMP_SYNTAX_NULL.

The WinSNMP application must release the resources associated with each variable bindings list. It should do this by matching each call to the 
<b>SnmpCreateVbl</b> and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a> functions with a corresponding call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<b>SnmpCreateVbl</b> or 
<b>SnmpDuplicateVbl</b>. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smioid">smiOID</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivalue">smiVALUE</a>