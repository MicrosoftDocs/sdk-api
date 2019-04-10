---
UID: NF:winsnmp.SnmpFreeVbl
title: SnmpFreeVbl function (winsnmp.h)
author: windows-sdk-content
description: The WinSNMP SnmpFreeVbl function releases resources associated with a variable bindings list. These are resources allocated previously by a call to the SnmpCreateVbl function or the SnmpDuplicateVbl function in a WinSNMP application.
old-location: snmp\snmpfreevbl.htm
tech.root: SNMP
ms.assetid: d9175523-bbf0-4e20-b4da-140a6ee0ebd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpFreeVbl, SnmpFreeVbl function [SNMP], _snmp_snmpfreevbl, snmp.snmpfreevbl, winsnmp/SnmpFreeVbl
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
 - SnmpFreeVbl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpFreeVbl function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpFreeVbl</b> function releases resources associated with a variable bindings list. These are resources allocated previously by a call to the 
<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a> function or the 
<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a> function in a WinSNMP application.


## -parameters




### -param vbl [in]

Handle to the variable bindings list to release.


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
<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a> and 
<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a> functions with a corresponding call to the 
<b>SnmpFreeVbl</b> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a> or 
<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a>.

If the application calls the 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> or the 
<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a> function, the Microsoft WinSNMP implementation frees all resources it allocates for the WinSNMP session. However, even if the application does not reuse a variable bindings list handle, it is recommended that the application free individual variable bindings resources with the 
<b>SnmpFreeVbl</b> function. This reduces the implementation's work load, and should enhance its service to all applications. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a>



<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a>



<a href="https://msdn.microsoft.com/5e973b32-3e7e-41f7-9257-4ac3d67fd853">SnmpCreateVbl</a>



<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

