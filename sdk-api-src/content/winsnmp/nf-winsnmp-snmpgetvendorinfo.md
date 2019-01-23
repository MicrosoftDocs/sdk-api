---
UID: NF:winsnmp.SnmpGetVendorInfo
title: SnmpGetVendorInfo function
author: windows-sdk-content
description: A WinSNMP application calls the SnmpGetVendorInfo function to retrieve information about the Microsoft WinSNMP implementation.
old-location: snmp\snmpgetvendorinfo.htm
tech.root: SNMP
ms.assetid: e5929fb9-5011-42b9-887e-db0ccdd79e2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpGetVendorInfo, SnmpGetVendorInfo function [SNMP], _snmp_snmpgetvendorinfo, snmp.snmpgetvendorinfo, winsnmp/SnmpGetVendorInfo
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpGetVendorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpGetVendorInfo function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpGetVendorInfo</b> function to retrieve information about the Microsoft WinSNMP implementation. The function returns the information in an 
<a href="https://msdn.microsoft.com/78b7b736-f68a-456a-9178-9a5b40e3bc8d">smiVENDORINFO</a> structure. The 
<b>SnmpGetVendorInfo</b> function is an element of the WinSNMP API, version 2.0.


## -parameters




### -param vendorInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/78b7b736-f68a-456a-9178-9a5b40e3bc8d">smiVENDORINFO</a> structure to receive information. The information includes a way to contact Microsoft and the enterprise number assigned to Microsoft by the Internet Assigned Numbers Authority (IANA).


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> specifying a <b>NULL</b> value in its <i>session</i> parameter. The 
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
<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a> function did not complete successfully.

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




<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/78b7b736-f68a-456a-9178-9a5b40e3bc8d">smiVENDORINFO</a>
 

 

