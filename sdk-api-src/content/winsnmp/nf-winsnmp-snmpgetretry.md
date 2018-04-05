---
UID: NF:winsnmp.SnmpGetRetry
title: SnmpGetRetry function
author: windows-driver-content
description: The WinSNMP SnmpGetRetry function returns the retry count value, in units, for the retransmission of SNMP message requests. The retry count applies to calls that a WinSNMP application makes to the SnmpSendMsg function for a specified management entity.
old-location: snmp\snmpgetretry.htm
old-project: SNMP
ms.assetid: 0c01994b-adce-4525-a41c-71cbe2fde2a8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpGetRetry, SnmpGetRetry function [SNMP], _snmp_snmpgetretry, snmp.snmpgetretry, winsnmp/SnmpGetRetry
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
-	SnmpGetRetry
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpGetRetry function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetRetry</b> function returns the retry count value, in units, for the retransmission of SNMP message requests. The retry count applies to calls that a WinSNMP application makes to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function for a specified management entity.


## -parameters




### -param hEntity [in]

Handle to the destination management entity of interest.


### -param nPolicyRetry [out]

Pointer to an unsigned long integer variable to receive the retry count value for the specified management entity. This is a value that the Microsoft WinSNMP implementation stores in a database. If you do not need the information returned in this parameter, <i>nPolicyRetry</i> must be a <b>NULL</b> pointer.


### -param nActualRetry [out]

Pointer to an unsigned long integer variable to receive the last actual or estimated retry count for the destination entity, as reported by the implementation. If you do not need the information returned in this parameter, <i>nActualRetry</i> must be a <b>NULL</b> pointer. If this parameter is a valid pointer, the function returns 0. For additional information, see the following Remarks section.


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
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The <i>nPolicyRetry</i> and <i>nActualRetry</i> parameters are both <b>NULL</b>. The operation was not performed.

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



Typically a WinSNMP application, rather than an agent application, calls the 
<b>SnmpGetRetry</b> function.

A WinSNMP application can modify the retry count value with a call to the 
<a href="https://msdn.microsoft.com/6a28ccc6-1d06-41d7-8d76-14e594102832">SnmpSetRetry</a> function.

The WinSNMP application can monitor the value of the <i>nActualRetry</i> parameter and compare it to the value of the <i>nPolicyRetry</i> parameter to optimize transmission performance. For additional information, see 
<a href="https://msdn.microsoft.com/71150a66-74a3-4957-bc70-3dd25c3b9c71">About Retransmission</a> and 
<a href="https://msdn.microsoft.com/1f1a9589-3566-4d90-ac4d-7acf69f34676">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://msdn.microsoft.com/8df40980-56e2-485f-87e0-42878b320e4e">SnmpGetRetransmitMode</a>



<a href="https://msdn.microsoft.com/d206ba15-a068-4579-bd6a-ab2444a723e0">SnmpSetRetransmitMode</a>



<a href="https://msdn.microsoft.com/6a28ccc6-1d06-41d7-8d76-14e594102832">SnmpSetRetry</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

