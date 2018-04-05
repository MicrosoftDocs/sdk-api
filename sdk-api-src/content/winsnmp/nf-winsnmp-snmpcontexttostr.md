---
UID: NF:winsnmp.SnmpContextToStr
title: SnmpContextToStr function
author: windows-driver-content
description: The WinSNMP SnmpContextToStr function returns a string that identifies an SNMP context, which is a set of managed object resources. The function returns the string in an smiOCTETS structure.
old-location: snmp\snmpcontexttostr.htm
old-project: SNMP
ms.assetid: d82c352d-8685-4276-b58c-ce89557f074a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpContextToStr, SnmpContextToStr function [SNMP], _snmp_snmpcontexttostr, snmp.snmpcontexttostr, winsnmp/SnmpContextToStr
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
req.typenames: SCARD_IO_REQUEST, *PSCARD_IO_REQUEST, *LPSCARD_IO_REQUEST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpContextToStr
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpContextToStr function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpContextToStr</b> function returns a string that identifies an SNMP context, which is a set of managed object resources. The function returns the string in an 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure.


## -parameters




### -param context [in]

Handle to the SNMP context of interest.


### -param string [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure to receive the string that identifies the context of interest. The string can have a null-terminating byte.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

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
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>context</i> parameter is invalid.

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



The current setting of the entity and context translation mode determines the type of output string 
<b>SnmpContextToStr</b> returns. For additional information, see 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application must provide the address of a valid 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure for the <i>string</i> parameter. If the 
<b>SnmpContextToStr</b> function completes successfully, the Microsoft WinSNMP implementation initializes the <b>len</b> and <b>ptr</b> members of the structure. The WinSNMP application must call the 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a> function to enable the implementation to free the resources for these members.

When the entity and context translation mode is SNMPAPI_TRANSLATED, and the entry exists in the implementation's database, the implementation returns the associated user-friendly name of the context. If an entry does not exist for the context name, 
<b>SnmpContextToStr</b> returns the SNMP community string.

When the entity and context translation mode is SNMPAPI_UNTRANSLATED_V1 or SNMPAPI_UNTRANSLATED_V2, the implementation also returns the SNMP community string.




## -see-also




<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a>
 

 

