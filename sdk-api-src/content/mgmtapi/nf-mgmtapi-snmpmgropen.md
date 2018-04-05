---
UID: NF:mgmtapi.SnmpMgrOpen
title: SnmpMgrOpen function
author: windows-driver-content
description: The SnmpMgrOpen function initializes communications sockets and data structures, allowing communications with the specified SNMP agent. This function is an element of the SNMP Management API.
old-location: snmp\snmpmgropen.htm
old-project: SNMP
ms.assetid: e2827352-f1aa-477e-933c-942c73cea487
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpMgrOpen, SnmpMgrOpen function [SNMP], _snmp_snmpmgropen, mgmtapi/SnmpMgrOpen, snmp.snmpmgropen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mgmtapi.h
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
req.typenames: SOURCE_GROUP_ENTRY, *PSOURCE_GROUP_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mgmtapi.dll
api_name:
-	SnmpMgrOpen
product: Windows
targetos: Windows
req.lib: Mgmtapi.lib
req.dll: Mgmtapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SnmpMgrOpen function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpMgrOpen</b> function initializes communications sockets and data structures, allowing communications with the specified SNMP agent. This function is an element of the SNMP Management API.


## -parameters




### -param lpAgentAddress [in]

Pointer to a <b>null</b>-terminated string that specifies a host name or an IP address. The host name must resolve to an IP address, an IPX address (in 8.12 notation), or an ethernet address. See the Remarks section for the acceptable forms for host names and IP addresses.


### -param lpAgentCommunity [in]

Pointer to a <b>null</b>-terminated string that specifies the SNMP community name to use when communicating with the agent that is identified by the <i>lpAgentAddress</i> parameter.


### -param nTimeOut [in]

Specifies the communications time-out in milliseconds.


### -param nRetries [in]

Specifies the communications retry count. The time-out that is specified in the <i>nTimeOut</i> parameter is doubled each time that a retry attempt is transmitted.


## -returns



If the function succeeds, the return value is a pointer to an <b>LPSNMP_MGR_SESSION</b> structure. This structure is used internally and the programmer should not alter it. For more information, see the following Remarks section.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> may return the SNMP_MEM_ALLOC_ERROR error code, which indicates a memory allocation error.

This function may also return Windows Sockets error codes.




## -remarks



If possible, use a host name to identify the SNMP agent in the <i>lpAgentAddress</i> parameter. Host names can be provided for agents only if TCP/IP is loaded and the names are TCP/IP host names. NetBIOS names cannot be supplied for IPX hosts.

The name and address of the SNMP target, or the string pointed to by the <i>lpAgentAddress</i> parameter, should conform to one of the following forms.
					

<table>
<tr>
<th>Name/Address</th>
<th>Form (example)</th>
</tr>
<tr>
<td>Host Name</td>
<td>merlin or merlin.microsoft.com</td>
</tr>
<tr>
<td>IPv4 Address</td>
<td>157.57.8.160</td>
</tr>
<tr>
<td>IPv6 Address</td>
<td>3ffe:8311:ffff::b3ff:fe88:c33</td>
</tr>
<tr>
<td>MAC Address</td>
<td>00aa00bbccdd</td>
</tr>
<tr>
<td>IPX Address</td>
<td>00006112.00aa00bbccdd</td>
</tr>
</table>
 

Applications should not use the <b>LPSNMP_MGR_SESSION</b> pointer that is returned by this function to call the 
<a href="https://msdn.microsoft.com/f66ce774-dba0-466b-ad1e-671f9a487e0f">SnmpMgrRequest</a> function in the context of a different thread.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/d8e7cc61-e313-4e36-88e7-686b4f9282b5">SnmpMgrClose</a>



<a href="https://msdn.microsoft.com/f66ce774-dba0-466b-ad1e-671f9a487e0f">SnmpMgrRequest</a>
 

 

