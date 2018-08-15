---
UID: NF:winsnmp.SnmpOidCopy
title: SnmpOidCopy function
author: windows-sdk-content
description: The WinSNMP SnmpOidCopy function copies an SNMP object identifier, allocating any necessary memory for the copy.
old-location: snmp\snmpoidcopy.htm
old-project: snmp
ms.assetid: ab121160-1c4f-41c0-a738-2e7605780ed2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SnmpOidCopy, SnmpOidCopy function [SNMP], _snmp_snmpoidcopy, snmp.snmpoidcopy, winsnmp/SnmpOidCopy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsnmp.h
req.include-header: 
req.redist: 
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
 - SnmpOidCopy
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpOidCopy function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpOidCopy</b> function copies an SNMP object identifier, allocating any necessary memory for the copy.


## -parameters




### -param srcOID [in]

Pointer to an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure to copy.


### -param dstOID [out]

Pointer to an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure to receive a copy of the object identifier specified by the <i>srcOID</i> parameter.


## -returns



If the function succeeds, the return value is the number of subidentifiers in the copied object identifier. This number is also the value of the <b>len</b> member of the 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure pointed to by the <i>dstOID</i> parameter.

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
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>srcOID</i> parameter is invalid.

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



On input, the 
<b>SnmpOidCopy</b> function ignores the members of the 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure pointed to by the <i>dstOID</i> parameter. The Microsoft WinSNMP implementation overwrites the 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> members if the function completes successfully.

The WinSNMP application must call the 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a> function to enable the implementation to free resources allocated for the <b>ptr</b> member of the 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure pointed to by the <i>dstOID</i> parameter. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a> and 
<a href="https://msdn.microsoft.com/3e4cbbc5-18bc-4731-971c-6e533d904f56">Freeing WinSNMP Descriptors</a>.




## -see-also




<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a>
 

 

