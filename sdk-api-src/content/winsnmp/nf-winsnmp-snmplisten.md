---
UID: NF:winsnmp.SnmpListen
title: SnmpListen function
author: windows-sdk-content
description: The WinSNMP SnmpListen function registers a WinSNMP application as an SNMP agent.
old-location: snmp\snmplisten.htm
old-project: SNMP
ms.assetid: e89c9315-efe4-4241-a7c4-f4475b107701
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpListen, SnmpListen function [SNMP], _snmp_snmplisten, snmp.snmplisten, winsnmp/SnmpListen
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
 - SnmpListen
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpListen function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpListen</b> function registers a WinSNMP application as an SNMP agent. An agent application calls this function to inform the Microsoft WinSNMP implementation that an entity will be acting in the role of an SNMP agent. An application also calls this function to inform the implementation when an entity will no longer be acting in this role. The 
<b>SnmpListen</b> function is an element of the WinSNMP API, version 2.0.


## -parameters




### -param hEntity [in]

Handle to the WinSNMP entity to notify when the Microsoft WinSNMP implementation receives an incoming SNMP request message (PDU). This parameter identifies the agent application. For more information, see the following Remarks and Return Values sections. 




When you call the 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> function, you can specify whether the implementation should use a window notification message or an 
<a href="https://msdn.microsoft.com/9871b4a8-c96c-48a7-9e7e-7fe1c259545e">SNMPAPI_CALLBACK</a> function to notify the application when an SNMP message or asynchronous event is available.


### -param lStatus [in]

Specifies an unsigned long integer variable that indicates whether the WinSNMP entity identified by the <i>hEntity</i> parameter is acting in an SNMP agent role, or if it is no longer acting in this role. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_ON"></a><a id="snmpapi_on"></a><dl>
<dt><b>SNMPAPI_ON</b></dt>
</dl>
</td>
<td width="60%">
The specified WinSNMP entity is functioning in an agent role.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The specified WinSNMP entity is not functioning in an agent role.

</td>
</tr>
</table>
 

Passing a value of SNMPAPI_OFF releases both the resources allocated to the entity and the port assigned it. For more information, see the following Remarks section.


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
<dt><b>SNMPAPI_MODE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lStatus</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>hEntity</i> parameter is already functioning in the role of an SNMP agent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_RESOURCE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
There is a network transport layer error. A socket could not be created for the entity specified by the <i>hEntity</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_OTHER</b></dt>
</dl>
</td>
<td width="60%">
An error occurred in the network transport layer while trying to bind a socket for the entity specified by the <i>hEntity</i> parameter.

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



When you specify an entity, you explicitly specify the address family, interface address, and port for the entity. This is because WinSNMP assigns these attributes to each WinSNMP entity as a result of a call to the 
<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a> function. The implementation uses the address and port settings currently assigned to the entity specified by the <i>hEntity</i> parameter when it sends notifications to the agent application. For more information, see 
<a href="https://msdn.microsoft.com/8b495a60-f1ef-4170-bf11-c98bb3dc857b">SnmpSetPort</a>.

When you call the 
<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a> function for a WinSNMP session and the 
<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a> function for a WinSNMP application, you must release all ports associated with WinSNMP agent applications.

For more information about SNMP management applications and agent applications, see 
<a href="https://msdn.microsoft.com/473560b5-4611-410e-aeae-764c9c76e765">Registering an SNMP Agent Application</a> and 
<a href="https://msdn.microsoft.com/55be55a8-1968-4373-a969-f7e03b75a824">About SNMP</a>.




## -see-also




<a href="https://msdn.microsoft.com/348f06e6-b408-4962-a0bc-8ff3e2ee21fa">SnmpCleanup</a>



<a href="https://msdn.microsoft.com/eac678f4-c77c-46b5-9c45-62b5822079da">SnmpClose</a>



<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/8b495a60-f1ef-4170-bf11-c98bb3dc857b">SnmpSetPort</a>



<a href="https://msdn.microsoft.com/d0a8e389-ba5b-45f4-9682-1fbe456daaed">SnmpStrToEntity</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

