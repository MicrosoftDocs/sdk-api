---
UID: NF:winsnmp.SnmpOidToStr
title: SnmpOidToStr function
author: windows-sdk-content
description: The WinSNMP SnmpOidToStr function converts the internal binary representation of an SNMP object identifier to its dotted numeric string format, for example, to &#0034;1.2.3.4.5.6&#0034;.
old-location: snmp\snmpoidtostr.htm
old-project: snmp
ms.assetid: 20f0af32-8f4f-4326-ab6a-389dc95be73f
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: SnmpOidToStr, SnmpOidToStr function [SNMP], _snmp_snmpoidtostr, snmp.snmpoidtostr, winsnmp/SnmpOidToStr
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
 - SnmpOidToStr
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpOidToStr function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpOidToStr</b> function converts the internal binary representation of an SNMP object identifier to its dotted numeric string format, for example, to "1.2.3.4.5.6".


## -parameters




### -param srcOID [in]

Pointer to an 
<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a> structure with an object identifier to convert.


### -param size [in]

Specifies the size, in bytes, of the buffer indicated by the <i>string</i> parameter. For more information, see the following Remarks section.


### -param string [out]

Pointer to a buffer to receive the converted string object identifier that specifies the SNMP management entity.


## -returns



If the function succeeds, the return value is the length, in bytes, of the string that the WinSNMP application writes to the <i>string</i> parameter. The return value includes a <b>null</b>-terminating byte. This value may be less than or equal to the value of the <i>size</i> parameter, but it may not be greater.

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
<dt><b>SNMPAPI_SIZE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>size</i> parameter is invalid. This parameter cannot be equal to zero; it must indicate the size of the buffer pointed to by the <i>string</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OID_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>srcOID</i> parameter is invalid. For additional information, see the following Remarks section.

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



It is recommended that a WinSNMP application specify, with the <i>size</i> parameter, a string buffer of MAXOBJIDSTRSIZE length (1408 bytes). This ensures that the output buffer is large enough to hold the converted string. Because the converted string is usually less than MAXOBJIDSTRSIZE, the WinSNMP application can copy the converted string to a smaller buffer. The application can then reuse or free the memory that it allocated for the initial buffer. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/cbcf8fc6-c5d6-476b-9490-4b87fd6a8a56">SnmpStrToOid</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/0bdf900e-6e67-4461-97bc-4c9650d888bf">smiOID</a>
 

 

