---
UID: NF:winsnmp.SnmpSetTimeout
title: SnmpSetTimeout function
author: windows-sdk-content
description: The WinSNMP SnmpSetTimeout function enables a WinSNMP application to change the time-out value for the transmission of SNMP message requests.
old-location: snmp\snmpsettimeout.htm
old-project: SNMP
ms.assetid: ae72f775-9f2a-4c16-b866-14ab17fd3a6a
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpSetTimeout, SnmpSetTimeout function [SNMP], _snmp_snmpsettimeout, snmp.snmpsettimeout, winsnmp/SnmpSetTimeout
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
-	SnmpSetTimeout
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpSetTimeout function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetTimeout</b> function enables a WinSNMP application to change the time-out value for the transmission of SNMP message requests. The time-out value applies to calls that a WinSNMP application makes to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function for a specified management entity. The Microsoft WinSNMP implementation stores the value in a database.


## -parameters




### -param hEntity [in]

Handle to the destination management entity of interest.


### -param nPolicyTimeout [in]

Specifies a new time-out value, in hundredths of a second, for the management entity. This value replaces the value currently stored in the implementation's database. 




If this parameter is equal to zero, and the current retransmission mode is equal to SNMPAPI_ON, the implementation selects a time-out value. The implementation uses this time-out value when it executes the WinSNMP application's retransmission policy.


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
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEntity</i> parameter is invalid.

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



Typically a WinSNMP manager application, rather than an agent application, calls the 
<b>SnmpSetTimeout</b> function.

For additional information, see 
<a href="https://msdn.microsoft.com/71150a66-74a3-4957-bc70-3dd25c3b9c71">About Retransmission</a> and 
<a href="https://msdn.microsoft.com/1f1a9589-3566-4d90-ac4d-7acf69f34676">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://msdn.microsoft.com/8df40980-56e2-485f-87e0-42878b320e4e">SnmpGetRetransmitMode</a>



<a href="https://msdn.microsoft.com/95f7afad-241c-473a-8041-3d1642f9d1fe">SnmpGetTimeout</a>



<a href="https://msdn.microsoft.com/d206ba15-a068-4579-bd6a-ab2444a723e0">SnmpSetRetransmitMode</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

