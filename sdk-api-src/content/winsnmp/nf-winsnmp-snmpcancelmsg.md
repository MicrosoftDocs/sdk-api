---
UID: NF:winsnmp.SnmpCancelMsg
title: SnmpCancelMsg function
author: windows-sdk-content
description: A WinSNMP application calls the SnmpCancelMsg function to request that the Microsoft WinSNMP implementation cancel retransmission attempts and time-out notifications for an SNMP request message.
old-location: snmp\snmpcancelmsg.htm
old-project: SNMP
ms.assetid: 018ad1b6-6f59-4c5d-813b-734ec8ced28a
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: SnmpCancelMsg, SnmpCancelMsg function [SNMP], _snmp_snmpcancelmsg, snmp.snmpcancelmsg, winsnmp/SnmpCancelMsg
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
-	SnmpCancelMsg
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpCancelMsg function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpCancelMsg</b> function to request that the Microsoft WinSNMP implementation cancel retransmission attempts and time-out notifications for an SNMP request message. The 
<b>SnmpCancelMsg</b> function is an element of the WinSNMP API, version 2.0.


## -parameters




### -param session [in]

Handle to the WinSNMP session that submitted the SNMP request message (PDU) to be canceled.


### -param reqId [in]

Specifies a unique numeric value that identifies the PDU of interest. This parameter must match the request identifier (<b>request_id</b>) of the <i>PDU</i> parameter specified in the application's initial call to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function.


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
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>reqId</i> parameter does not identify an outstanding message for the specified session.

</td>
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



Calling the 
<b>SnmpCancelMsg</b> function is equivalent to calling the 
<a href="https://msdn.microsoft.com/d206ba15-a068-4579-bd6a-ab2444a723e0">SnmpSetRetransmitMode</a> function, for a specific SNMP message, with the retransmission mode equal to SNMPAPI_OFF.

For more information, see 
<a href="https://msdn.microsoft.com/3fd39425-7d57-4bbb-9dcb-f43b6211228c">Canceling Retransmission</a> and 
<a href="https://msdn.microsoft.com/1f1a9589-3566-4d90-ac4d-7acf69f34676">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/d206ba15-a068-4579-bd6a-ab2444a723e0">SnmpSetRetransmitMode</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

