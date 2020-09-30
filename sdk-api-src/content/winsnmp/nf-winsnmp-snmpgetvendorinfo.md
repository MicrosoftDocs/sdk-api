---
UID: NF:winsnmp.SnmpGetVendorInfo
title: SnmpGetVendorInfo function (winsnmp.h)
description: A WinSNMP application calls the SnmpGetVendorInfo function to retrieve information about the Microsoft WinSNMP implementation.
helpviewer_keywords: ["SnmpGetVendorInfo","SnmpGetVendorInfo function [SNMP]","_snmp_snmpgetvendorinfo","snmp.snmpgetvendorinfo","winsnmp/SnmpGetVendorInfo"]
old-location: snmp\snmpgetvendorinfo.htm
tech.root: SNMP
ms.assetid: e5929fb9-5011-42b9-887e-db0ccdd79e2b
ms.date: 12/05/2018
ms.keywords: SnmpGetVendorInfo, SnmpGetVendorInfo function [SNMP], _snmp_snmpgetvendorinfo, snmp.snmpgetvendorinfo, winsnmp/SnmpGetVendorInfo
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
 - SnmpGetVendorInfo
 - winsnmp/SnmpGetVendorInfo
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
 - SnmpGetVendorInfo
---

# SnmpGetVendorInfo function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpGetVendorInfo</b> function to retrieve information about the Microsoft WinSNMP implementation. The function returns the information in an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivendorinfo">smiVENDORINFO</a> structure. The 
<b>SnmpGetVendorInfo</b> function is an element of the WinSNMP API, version 2.0.

## -parameters

### -param vendorInfo [out]

Pointer to an 
<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivendorinfo">smiVENDORINFO</a> structure to receive information. The information includes a way to contact Microsoft and the enterprise number assigned to Microsoft by the Internet Assigned Numbers Authority (IANA).

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
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The <i>vendorInfo</i> parameter is <b>NULL</b>.

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

## -see-also

<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>



<a href="/windows/desktop/api/winsnmp/ns-winsnmp-smivendorinfo">smiVENDORINFO</a>