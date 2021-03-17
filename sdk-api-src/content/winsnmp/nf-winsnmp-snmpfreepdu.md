---
UID: NF:winsnmp.SnmpFreePdu
title: SnmpFreePdu function (winsnmp.h)
description: The WinSNMP SnmpFreePdu function releases resources associated with an SNMP protocol data unit (PDU) created by the SnmpCreatePdu or the SnmpDuplicatePdu function.
helpviewer_keywords: ["SnmpFreePdu","SnmpFreePdu function [SNMP]","_snmp_snmpfreepdu","snmp.snmpfreepdu","winsnmp/SnmpFreePdu"]
old-location: snmp\snmpfreepdu.htm
tech.root: SNMP
ms.assetid: 243e52aa-2b05-4c41-9f89-cf9c66517da6
ms.date: 12/05/2018
ms.keywords: SnmpFreePdu, SnmpFreePdu function [SNMP], _snmp_snmpfreepdu, snmp.snmpfreepdu, winsnmp/SnmpFreePdu
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
 - SnmpFreePdu
 - winsnmp/SnmpFreePdu
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
 - SnmpFreePdu
---

# SnmpFreePdu function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpFreePdu</b> function releases resources associated with an SNMP protocol data unit (PDU) created by the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatepdu">SnmpCreatePdu</a> or the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpduplicatepdu">SnmpDuplicatePdu</a> function.

## -parameters

### -param PDU [in]

Handle to the SNMP PDU to free.

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
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The PDU handle is invalid.

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

If the application calls the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a> or the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a> function, the Microsoft WinSNMP implementation frees all resources it allocates for the WinSNMP session. However, it is recommended that the application free individual resources with the WinSNMP function that corresponds to the resource. This reduces the implementation's work load, and should enhance the implementation's service to all applications. The application should use the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a> function to deallocate variable bindings list resources. For additional information, see 
<a href="/windows/desktop/SNMP/winsnmp-data-management-concepts">WinSNMP Data Management Concepts</a>.

Under WinSNMP, a variable binding entry exists only within a variable bindings list, even if the variable bindings list contains just one entry.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcleanup">SnmpCleanup</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpclose">SnmpClose</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreevbl">SnmpFreeVbl</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>