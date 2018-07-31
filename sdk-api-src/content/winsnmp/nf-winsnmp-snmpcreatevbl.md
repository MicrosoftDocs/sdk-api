---
UID: NF:winsnmp.SnmpCreateVbl
title: SnmpCreateVbl function
author: windows-sdk-content
description: The WinSNMP SnmpCreateVbl function creates a new variable bindings list for the calling WinSNMP application.
old-location: snmp\snmpcreatevbl.htm
old-project: SNMP
ms.assetid: 5e973b32-3e7e-41f7-9257-4ac3d67fd853
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SnmpCreateVbl, SnmpCreateVbl function [SNMP], _snmp_snmpcreatevbl, snmp.snmpcreatevbl, winsnmp/SnmpCreateVbl
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
 - SnmpCreateVbl
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpCreateVbl function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpCreateVbl</b> function creates a new variable bindings list for the calling WinSNMP application. If the <i>name</i> and <i>value</i> parameters are not <b>NULL</b>, 
<b>SnmpCreateVbl</b> uses their values to create the first variable binding entry for the new variable bindings list. The 
<b>SnmpCreateVbl</b> function returns a handle to the new variable bindings list and allocates any necessary memory for it.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param name [in]

Pointer to an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure that contains the variable name for the first variable binding entry. This parameter can be <b>NULL</b>. For additional information, see the following Remarks section.


### -param value [in]

Pointer to an 
<a href="https://msdn.microsoft.com/e5e8f321-54b2-469d-bdd3-9867fd85b447">smiVALUE</a> structure that contains a value to associate with the variable in the first variable binding entry. This parameter can be <b>NULL</b>. For additional information, see the following Remarks section.


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
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>name</i> parameter references an invalid 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure.

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
<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a> functions with a corresponding call to the 
<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a> function. To avoid memory leaks, a WinSNMP application must call 
<b>SnmpFreeVbl</b> before it reuses the handle to a variable bindings list in a subsequent call to 
<b>SnmpCreateVbl</b> or 
<b>SnmpDuplicateVbl</b>. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/b6ca0167-43d7-4a85-b3ba-c2683ae27ff5">SnmpDuplicateVbl</a>



<a href="https://msdn.microsoft.com/d9175523-bbf0-4e20-b4da-140a6ee0ebd4">SnmpFreeVbl</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a>



<a href="https://msdn.microsoft.com/e5e8f321-54b2-469d-bdd3-9867fd85b447">smiVALUE</a>
 

 

