---
UID: NF:winsnmp.SnmpCountVbl
title: SnmpCountVbl function
author: windows-sdk-content
description: A WinSNMP application calls the WinSNMP SnmpCountVbl function to enumerate the variable binding entries in the specified variable bindings list.
old-location: snmp\snmpcountvbl.htm
old-project: SNMP
ms.assetid: 08e7d450-0c75-4ef5-a9c5-ef0255601a9a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SnmpCountVbl, SnmpCountVbl function [SNMP], _snmp_snmpcountvbl, snmp.snmpcountvbl, winsnmp/SnmpCountVbl
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpCountVbl
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpCountVbl function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the WinSNMP 
<b>SnmpCountVbl</b> function to enumerate the variable binding entries in the specified variable bindings list.


## -parameters




### -param vbl [in]

Handle to the variable bindings list to enumerate.


## -returns



If the function succeeds, the return value is the count of variable binding entries in the variable bindings list.

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
<a href="https://msdn.microsoft.com/a6598b4e-6797-4e18-8ab5-059c75bc84ef">SnmpGetVb</a>, 
<a href="https://msdn.microsoft.com/65d962bd-f4d7-4cf4-9b24-a7678e669e24">SnmpSetVb</a>, and 
<a href="https://msdn.microsoft.com/b6f8a61a-493c-4626-9134-f8badce678c4">SnmpDeleteVb</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/b6f8a61a-493c-4626-9134-f8badce678c4">SnmpDeleteVb</a>



<a href="https://msdn.microsoft.com/a6598b4e-6797-4e18-8ab5-059c75bc84ef">SnmpGetVb</a>



<a href="https://msdn.microsoft.com/65d962bd-f4d7-4cf4-9b24-a7678e669e24">SnmpSetVb</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

