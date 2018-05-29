---
UID: NF:winsnmp.SnmpEntityToStr
title: SnmpEntityToStr function
author: windows-sdk-content
description: The WinSNMP SnmpEntityToStr function returns a string that identifies an SNMP management entity.
old-location: snmp\snmpentitytostr.htm
old-project: SNMP
ms.assetid: 3a5bca7e-a0a2-4bf5-86cc-f8d9f3ac8660
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpEntityToStr, SnmpEntityToStr function [SNMP], _snmp_snmpentitytostr, snmp.snmpentitytostr, winsnmp/SnmpEntityToStr
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpEntityToStr
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpEntityToStr function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpEntityToStr</b> function returns a string that identifies an SNMP management entity.


## -parameters




### -param entity [in]

Handle to the SNMP management entity of interest.


### -param size [in]

Specifies the size, in bytes, of the buffer pointed to by the <i>string</i> parameter. The WinSNMP application must allocate a buffer that is large enough to contain the output string.


### -param string [out]

Pointer to a buffer to receive the null-terminated string that identifies the SNMP management entity of interest.


## -returns



If the function succeeds, the return value is the number of bytes, including a terminating null byte, that 
<b>SnmpEntityToStr</b> returns in the <i>string</i> buffer. This value can be less than or equal to the value of the <i>size</i> parameter, but it cannot be greater.

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
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>entity</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OUTPUT_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The output buffer length is insufficient.

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
<b>SnmpEntityToStr</b> returns. For additional information, see 
<a href="https://msdn.microsoft.com/b90b8e95-dab0-483b-9336-07e20c122cba">Support for IPX Address Strings in WinSNMP</a> and 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a>.

When the entity and context translation mode is SNMPAPI_TRANSLATED, and an entry exists in the implementation's database, the implementation returns the associated user-friendly name of the management entity. If an entry does not exist for the management entity, 
<b>SnmpEntityToStr</b> returns the literal SNMP transport address of the management entity.

When the entity and context translation mode is SNMPAPI_UNTRANSLATED_V1 or SNMPAPI_UNTRANSLATED_V2, the Microsoft WinSNMP implementation also returns the literal SNMP transport address of the management entity.




## -see-also




<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

