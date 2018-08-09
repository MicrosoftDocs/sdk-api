---
UID: NF:winsnmp.SnmpSetTranslateMode
title: SnmpSetTranslateMode function
author: windows-sdk-content
description: The WinSNMP SnmpSetTranslateMode function enables a WinSNMP application to change the entity and context translation mode. The entity and context translation mode affects the interpretation and return of WinSNMP input and output string parameters.
old-location: snmp\snmpsettranslatemode.htm
old-project: snmp
ms.assetid: 8ee7e660-e718-40e6-adcd-1554eb7391d9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SNMPAPI_TRANSLATED, SNMPAPI_UNTRANSLATED_V1, SNMPAPI_UNTRANSLATED_V2, SnmpSetTranslateMode, SnmpSetTranslateMode function [SNMP], _snmp_snmpsettranslatemode, snmp.snmpsettranslatemode, winsnmp/SnmpSetTranslateMode
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
 - SnmpSetTranslateMode
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpSetTranslateMode function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetTranslateMode</b> function enables a WinSNMP application to change the entity and context translation mode. The entity and context translation mode affects the interpretation and return of WinSNMP input and output string parameters.


## -parameters




### -param nTranslateMode [in]

Specifies a value for the new entity and context translation mode. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_TRANSLATED"></a><a id="snmpapi_translated"></a><dl>
<dt><b>SNMPAPI_TRANSLATED</b></dt>
</dl>
</td>
<td width="60%">
The Microsoft WinSNMP implementation uses its database to translate user-friendly names for SNMP entities and managed objects. The implementation translates them into their SNMPv1 or SNMPv2C components.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V1"></a><a id="snmpapi_untranslated_v1"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V1</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of zero in the version field.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_UNTRANSLATED_V2"></a><a id="snmpapi_untranslated_v2"></a><dl>
<dt><b>SNMPAPI_UNTRANSLATED_V2</b></dt>
</dl>
</td>
<td width="60%">
The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters as SNMP community strings. For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of 1 in the version field.

</td>
</tr>
</table>
 


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
<dt><b>SNMPAPI_MODE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The implementation does not support the requested translation mode.

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



The new entity and context translation mode affects subsequent calls to the 
<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>, 
<a href="https://msdn.microsoft.com/d552f453-cc19-4166-aca3-bbaa3669b1c8">SnmpStrToContext</a>, 
<a href="https://msdn.microsoft.com/d82c352d-8685-4276-b58c-ce89557f074a">SnmpContextToStr</a>, and 
<a href="https://msdn.microsoft.com/3a5bca7e-a0a2-4bf5-86cc-f8d9f3ac8660">SnmpEntityToStr</a> functions. The WinSNMP application can change the entity and context translation mode again by making another call to 
<b>SnmpSetTranslateMode</b> with a different <i>nTranslateMode</i> value.

For additional information, see 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.




## -see-also




<a href="https://msdn.microsoft.com/d82c352d-8685-4276-b58c-ce89557f074a">SnmpContextToStr</a>



<a href="https://msdn.microsoft.com/3a5bca7e-a0a2-4bf5-86cc-f8d9f3ac8660">SnmpEntityToStr</a>



<a href="https://msdn.microsoft.com/244bddc1-37fc-4f5b-a1d0-99fd7a76c7a2">SnmpGetTranslateMode</a>



<a href="https://msdn.microsoft.com/d552f453-cc19-4166-aca3-bbaa3669b1c8">SnmpStrToContext</a>



<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

