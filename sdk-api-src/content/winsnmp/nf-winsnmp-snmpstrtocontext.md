---
UID: NF:winsnmp.SnmpStrToContext
title: SnmpStrToContext function
author: windows-driver-content
description: The WinSNMP SnmpStrToContext function returns a handle to SNMP context information that is specific to the Microsoft WinSNMP implementation.
old-location: snmp\snmpstrtocontext.htm
old-project: SNMP
ms.assetid: d552f453-cc19-4166-aca3-bbaa3669b1c8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpStrToContext, SnmpStrToContext function [SNMP], _snmp_snmpstrtocontext, snmp.snmpstrtocontext, winsnmp/SnmpStrToContext
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
-	SnmpStrToContext
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpStrToContext function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpStrToContext</b> function returns a handle to SNMP context information that is specific to the Microsoft WinSNMP implementation. The handle is a valid value that a WinSNMP application can use as the <i>context</i> parameter in a call to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> and 
<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a> functions.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param string [in]

Pointer to an 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure that contains a string to interpret. The string can identify a collection of managed objects, or it can be a community string. 




The current setting of the entity and context translation mode determines the way 
<b>SnmpStrToContext</b> interprets the input string structure as shown in the following table.

<table>
<tr>
<th>Entity/Context Translation Mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_TRANSLATED"></a><a id="snmpapi_translated"></a><dl>
<dt><b>SNMPAPI_TRANSLATED</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a user-friendly name for a collection of managed objects. The implementation translates the name into its SNMPv1 or SNMPv2C components using the implementation's database.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP community string.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets the <i>string</i> parameter as a literal SNMP community string.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a handle to the context of interest.

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
The <i>session</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>string</i> parameter format is invalid. For example, the <b>len</b> member or the <b>ptr</b> member of the 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure pointed to by the <i>string</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The value referenced in the <i>string</i> parameter does not exist.

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



The current setting of the entity and context translation mode determines the manner in which 
<b>SnmpStrToContext</b> interprets the input string structure. For additional information, see 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.

The WinSNMP application must call the 
<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a> function to release the context handle allocated by the 
<b>SnmpStrToContext</b> function. For additional information about releasing resources, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.

The WinSNMP application should free the memory associated with the <b>ptr</b> member of the 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure pointed to by the <i>string</i> parameter. This is because the application defines and allocates the resources. For example, if the application allocated resources with a call to the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> function, it should use the 
<a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> function to deallocate the resources. For additional information, see 
<a href="https://msdn.microsoft.com/3e4cbbc5-18bc-4731-971c-6e533d904f56">Freeing WinSNMP Descriptors</a>.




## -see-also




<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>



<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a>
 

 

