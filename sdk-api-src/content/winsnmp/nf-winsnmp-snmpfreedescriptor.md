---
UID: NF:winsnmp.SnmpFreeDescriptor
title: SnmpFreeDescriptor function
author: windows-driver-content
description: A WinSNMP application uses the SnmpFreeDescriptor function to inform the Microsoft WinSNMP implementation that it no longer requires access to a descriptor object.
old-location: snmp\snmpfreedescriptor.htm
old-project: SNMP
ms.assetid: 535f728d-6964-47b6-9913-7cd38356053d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpFreeDescriptor, SnmpFreeDescriptor function [SNMP], _snmp_snmpfreedescriptor, snmp.snmpfreedescriptor, winsnmp/SnmpFreeDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpFreeDescriptor
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpFreeDescriptor function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application uses the 
<b>SnmpFreeDescriptor</b> function to inform the Microsoft WinSNMP implementation that it no longer requires access to a descriptor object. This WinSNMP function signals the implementation to free the memory it allocated for the descriptor object.


## -parameters




### -param syntax [in]

Specifies the syntax data type of the target descriptor object.


### -param descriptor [in]

Pointer to an <b>smiOPAQUE</b> structure that contains the target descriptor object to release.


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
<dt><b>SNMPAPI_SYNTAX_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>syntax</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>descriptor</i> parameter is invalid. For additional information, see the following Remarks section.

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



The implementation allocates and deallocates memory for output descriptor objects with variable lengths. This memory allocation and deallocation are restricted to the implementation, except for the interface that the 
<b>SnmpFreeDescriptor</b> function provides. For additional information, see 
<a href="https://msdn.microsoft.com/3e4cbbc5-18bc-4731-971c-6e533d904f56">Freeing WinSNMP Descriptors</a>.

The implementation returns the SNMPAPI_OPERATION_INVALID error code if the <i>descriptor</i> parameter specifies a memory allocation that the implementation released in a prior call to 
<b>SnmpFreeDescriptor</b>. The function returns the same error code if the <i>descriptor</i> parameter specifies a memory allocation that the implementation did not make for the calling WinSNMP application.




## -see-also




<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>



<a href="https://msdn.microsoft.com/ab121160-1c4f-41c0-a738-2e7605780ed2">SnmpOidCopy</a>



<a href="https://msdn.microsoft.com/cbcf8fc6-c5d6-476b-9490-4b87fd6a8a56">SnmpStrToOid</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

