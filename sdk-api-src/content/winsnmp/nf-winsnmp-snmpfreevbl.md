---
UID: NF:winsnmp.SnmpFreeVbl
title: SnmpFreeVbl function (winsnmp.h)
description: The WinSNMP SnmpFreeVbl function releases resources associated with a variable bindings list. These are resources allocated previously by a call to the SnmpCreateVbl function or the SnmpDuplicateVbl function in a WinSNMP application.
helpviewer_keywords: ["SnmpFreeVbl","SnmpFreeVbl function [SNMP]","_snmp_snmpfreevbl","snmp.snmpfreevbl","winsnmp/SnmpFreeVbl"]
old-location: snmp\snmpfreevbl.htm
tech.root: SNMP
ms.assetid: d9175523-bbf0-4e20-b4da-140a6ee0ebd4
ms.date: 12/05/2018
ms.keywords: SnmpFreeVbl, SnmpFreeVbl function [SNMP], _snmp_snmpfreevbl, snmp.snmpfreevbl, winsnmp/SnmpFreeVbl
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
 - SnmpFreeVbl
 - winsnmp/SnmpFreeVbl
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
 - SnmpFreeVbl
---

# SnmpFreeVbl function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpFreeVbl</b> function releases resources associated with a variable bindings list. These are resources allocated previously by a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a> function or the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a> function in a WinSNMP application.

## -parameters

### -param vbl [in]

Handle to the variable bindings list to release.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS.

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

The WinSNMP application must release the resources associated with each variable bindings list. It should do this by matching each call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a> and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a> functions with a corresponding call to the 
<b>SnmpFreeVbl</b> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a> or 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a>.

If the application calls the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> or the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> function, the Microsoft WinSNMP implementation frees all resources it allocates for the WinSNMP session. However, even if the application does not reuse a variable bindings list handle, it is recommended that the application free individual variable bindings resources with the 
<b>SnmpFreeVbl</b> function. This reduces the implementation's work load, and should enhance its service to all applications. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatevbl">SnmpCreateVbl</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatevbl">SnmpDuplicateVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>