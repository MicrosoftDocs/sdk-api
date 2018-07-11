---
UID: NF:winsnmp.SnmpDuplicateVbl
title: SnmpDuplicateVbl function
author: windows-sdk-content
description: The WinSNMP SnmpDuplicateVbl function copies a variable bindings list for the specified WinSNMP session. This function returns a handle to the copied variable bindings list and allocates any necessary memory for it.
old-location: snmp\snmpduplicatevbl.htm
old-project: snmp
ms.assetid: b6ca0167-43d7-4a85-b3ba-c2683ae27ff5
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: SnmpDuplicateVbl, SnmpDuplicateVbl function [SNMP], _snmp_snmpduplicatevbl, snmp.snmpduplicatevbl, winsnmp/SnmpDuplicateVbl
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
 - SnmpDuplicateVbl
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpDuplicateVbl function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

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
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
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
<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a> and 
<b>SnmpDuplicateVbl</b> functions with a corresponding call to the 
<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<b>SnmpCreateVbl</b> or 
<b>SnmpDuplicateVbl</b>. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a>



<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

