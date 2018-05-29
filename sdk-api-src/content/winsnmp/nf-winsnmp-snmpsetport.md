---
UID: NF:winsnmp.SnmpSetPort
title: SnmpSetPort function
author: windows-sdk-content
description: A WinSNMP application calls the SnmpSetPort function to change the port assigned to a destination entity. The SnmpSetPort function is an element of the WinSNMP API, version 2.0.
old-location: snmp\snmpsetport.htm
old-project: SNMP
ms.assetid: 8b495a60-f1ef-4170-bf11-c98bb3dc857b
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpSetPort, SnmpSetPort function [SNMP], _snmp_snmpsetport, snmp.snmpsetport, winsnmp/SnmpSetPort
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
-	SnmpSetPort
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpSetPort function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpSetPort</b> function to change the port assigned to a destination entity. The 
<b>SnmpSetPort</b> function is an element of the WinSNMP API, version 2.0.


## -parameters




### -param hEntity [in]

Handle to a WinSNMP destination entity. This parameter can specify the handle to an entity acting in the role of an SNMP agent application as a result of a call to the 
<a href="https://msdn.microsoft.com/e89c9315-efe4-4241-a7c4-f4475b107701">SnmpListen</a> function. For more information, see the following Remarks section.


### -param nPort [in]

Specifies an unsigned integer that identifies the new port assignment for the destination entity. If you specify a local address that is busy, or if you specify a remote address that is unavailable, a call to the 
<b>SnmpSetPort</b> function fails.


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
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>hEntity</i> parameter is already functioning in an agent role as the result of a call to the 
<a href="https://msdn.microsoft.com/e89c9315-efe4-4241-a7c4-f4475b107701">SnmpListen</a> function. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEntity</i> parameter is invalid. This parameter must be a handle returned by a previous call to the 
<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a> function.

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



The Microsoft WinSNMP implementation assigns a port to each management entity as a result of a WinSNMP application's call to the 
<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a> function. If the SNMPAPI_UNTRANSLATED mode is in effect when the implementation creates an entity, the implementation typically assigns the standard SNMP request port for the respective protocol family to the entity; for example, UDP 161 or IPX 36879. If the SNMPAPI_TRANSLATED mode is in effect, the implementation assigns the port specified for the entity in the WinSNMP database. To retrieve the current entity and context translation mode in effect for the implementation, an application can call the 
<a href="https://msdn.microsoft.com/244bddc1-37fc-4f5b-a1d0-99fd7a76c7a2">SnmpGetTranslateMode</a> function. For more information, see 
<a href="https://msdn.microsoft.com/2550f235-1351-440a-8b4e-f0d30b058229">Setting the Entity and Context Translation Mode</a> and 
<a href="https://msdn.microsoft.com/0a0d9731-d800-4eaa-8230-25469a0b0285">The WinSNMP Database</a>.

A call to the 
<b>SnmpSetPort</b> function fails if the entity specified by the <i>hEntity</i> parameter is currently functioning in an agent role. This is because the entity has already been assigned to a port other than the one specified by the <i>nPort</i> parameter. To ensure assignment of an agent application to a specific port, a WinSNMP application can perform the following steps.

<ol>
<li>
Call <a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a> as follows:

<code>hAgent = SnmpStrToEntity (hSession, &lt;addrString&gt;);</code>

</li>
<li>
Call <b>SnmpSetPort</b> as follows: 

<code>SnmpSetPort (hAgent, &lt;nPort&gt;);</code>

</li>
<li>
Call <a href="https://msdn.microsoft.com/e89c9315-efe4-4241-a7c4-f4475b107701">SnmpListen</a> as follows:

<code>SnmpListen (hAgent, SNMPAPI_ON);</code>

</li>
</ol>
where &lt;addrString&gt; contains the string representation of an IP address or an IPX address, and &lt;nPort&gt; contains the new port assignment for the agent application.

Note that an IPX address contains a network number that consists of eight hexadecimal digits (zero-filled if necessary); a separator (either ":", "." or " – "); and a node number that consists of 12 hexadecimal digits (zero-filled if necessary)—for example, 00000001:00081A0D01C2. For more information, see 
<a href="https://msdn.microsoft.com/b90b8e95-dab0-483b-9336-07e20c122cba">Support for IPX Address Strings in WinSNMP</a>.




## -see-also




<a href="https://msdn.microsoft.com/244bddc1-37fc-4f5b-a1d0-99fd7a76c7a2">SnmpGetTranslateMode</a>



<a href="https://msdn.microsoft.com/e89c9315-efe4-4241-a7c4-f4475b107701">SnmpListen</a>



<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

