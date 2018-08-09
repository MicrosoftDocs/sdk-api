---
UID: NF:winsnmp.SnmpGetRetransmitMode
title: SnmpGetRetransmitMode function
author: windows-sdk-content
description: The WinSNMP SnmpGetRetransmitMode function returns the current setting of the retransmission mode to a WinSNMP application.
old-location: snmp\snmpgetretransmitmode.htm
old-project: snmp
ms.assetid: 8df40980-56e2-485f-87e0-42878b320e4e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpGetRetransmitMode, SnmpGetRetransmitMode function [SNMP], _snmp_snmpgetretransmitmode, snmp.snmpgetretransmitmode, winsnmp/SnmpGetRetransmitMode
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
 - SnmpGetRetransmitMode
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpGetRetransmitMode function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpGetRetransmitMode</b> function returns the current setting of the retransmission mode to a WinSNMP application. The Microsoft WinSNMP implementation uses the retransmission mode to govern transmission time-outs and retransmission attempts on calls to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function.


## -parameters




### -param nRetransmitMode [out]

Pointer to an unsigned long integer variable to receive the current retransmission mode in effect for the implementation. This parameter can be one of the following values. 



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
The implementation is executing the WinSNMP application's retransmission policy.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The implementation is not executing the WinSNMP application's retransmission policy.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. If 
<b>SnmpGetRetransmitMode</b> fails, the value of the <i>nRetransmitMode</i> parameter has no meaning for the application. To get extended error information, call 
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
<b>SnmpGetRetransmitMode</b> function. For additional information, see 
<a href="https://msdn.microsoft.com/71150a66-74a3-4957-bc70-3dd25c3b9c71">About Retransmission</a> and 
<a href="https://msdn.microsoft.com/1f1a9589-3566-4d90-ac4d-7acf69f34676">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://msdn.microsoft.com/d206ba15-a068-4579-bd6a-ab2444a723e0">SnmpSetRetransmitMode</a>



<a href="https://msdn.microsoft.com/7b8a4a1e-871f-424b-8bcb-c0b3bfaae9ce">SnmpStartup</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

