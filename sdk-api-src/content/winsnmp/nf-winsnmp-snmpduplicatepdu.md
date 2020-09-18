---
UID: NF:winsnmp.SnmpDuplicatePdu
title: SnmpDuplicatePdu function (winsnmp.h)
description: The WinSNMP SnmpDuplicatePdu function duplicates the SNMP protocol data unit (PDU) that the PDU parameter identifies, allocating any necessary memory for the duplicate PDU.
helpviewer_keywords: ["SnmpDuplicatePdu","SnmpDuplicatePdu function [SNMP]","_snmp_snmpduplicatepdu","snmp.snmpduplicatepdu","winsnmp/SnmpDuplicatePdu"]
old-location: snmp\snmpduplicatepdu.htm
tech.root: SNMP
ms.assetid: 4507cc9b-36a5-45bf-916d-9dc82ac381a5
ms.date: 12/05/2018
ms.keywords: SnmpDuplicatePdu, SnmpDuplicatePdu function [SNMP], _snmp_snmpduplicatepdu, snmp.snmpduplicatepdu, winsnmp/SnmpDuplicatePdu
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
 - SnmpDuplicatePdu
 - winsnmp/SnmpDuplicatePdu
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
 - SnmpDuplicatePdu
---

# SnmpDuplicatePdu function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDuplicatePdu</b> function duplicates the SNMP protocol data unit (PDU) that the <i>PDU</i> parameter identifies, allocating any necessary memory for the duplicate PDU.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param PDU [in]

Handle to the PDU to duplicate. The 
<b>SnmpDuplicatePdu</b> function provides a unique handle to each PDU within the calling application.

## -returns

If the function succeeds, the return value is a handle that identifies the new duplicate PDU.

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

To release resources allocated by the 
<b>SnmpDuplicatePdu</b> function for a new PDU, a WinSNMP application must call the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a> function.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetpdudata">SnmpGetPduData</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>