---
UID: NF:winsnmp.SnmpSetRetransmitMode
title: SnmpSetRetransmitMode function
author: windows-sdk-content
description: The WinSNMP SnmpSetRetransmitMode function enables a WinSNMP application to set the retransmission mode.
old-location: snmp\snmpsetretransmitmode.htm
old-project: SNMP
ms.assetid: d206ba15-a068-4579-bd6a-ab2444a723e0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SNMPAPI_OFF, SNMPAPI_ON, SnmpSetRetransmitMode, SnmpSetRetransmitMode function [SNMP], _snmp_snmpsetretransmitmode, snmp.snmpsetretransmitmode, winsnmp/SnmpSetRetransmitMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winsnmp.h
req.include-header: 
req.redist: 
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
 - SnmpSetRetransmitMode
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpSetRetransmitMode function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpSetRetransmitMode</b> function enables a WinSNMP application to set the retransmission mode. The Microsoft WinSNMP implementation uses the new retransmission mode to govern transmission time-outs and retransmission attempts on subsequent calls to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function.


## -parameters




### -param nRetransmitMode [in]

Specifies a value for the new retransmission mode. This parameter must be one of the following values. 



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
The implementation executes the WinSNMP application's retransmission policy.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMPAPI_OFF"></a><a id="snmpapi_off"></a><dl>
<dt><b>SNMPAPI_OFF</b></dt>
</dl>
</td>
<td width="60%">
The implementation does not execute the WinSNMP application's retransmission policy.

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
The implementation does not support the requested retransmission mode.

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
<b>SnmpSetRetransmitMode</b> function.

If a WinSNMP application sets the retransmission mode to SNMPAPI_OFF, the implementation does not initiate retransmission attempts for new SNMP communications operations. The new setting affects all subsequent calls to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function, until the WinSNMP application sets the retransmission mode back to SNMPAPI_ON.

Calling the 
<a href="https://msdn.microsoft.com/018ad1b6-6f59-4c5d-813b-734ec8ced28a">SnmpCancelMsg</a> function is equivalent to calling the 
<b>SnmpSetRetransmitMode</b> function, for a specific SNMP message, with the retransmission mode equal to SNMPAPI_OFF.

<div class="alert"><b>Note</b>  If the implementation returns the error SNMPAPI_MODE_INVALID to a call to 
<b>SnmpSetRetransmitMode</b>, the WinSNMP application must execute the retransmission policy.</div>
<div> </div>
For additional information, see 
<a href="https://msdn.microsoft.com/71150a66-74a3-4957-bc70-3dd25c3b9c71">About Retransmission</a> and 
<a href="https://msdn.microsoft.com/1f1a9589-3566-4d90-ac4d-7acf69f34676">Managing the Retransmission Policy</a>.




## -see-also




<a href="https://msdn.microsoft.com/018ad1b6-6f59-4c5d-813b-734ec8ced28a">SnmpCancelMsg</a>



<a href="https://msdn.microsoft.com/8df40980-56e2-485f-87e0-42878b320e4e">SnmpGetRetransmitMode</a>



<a href="https://msdn.microsoft.com/0c01994b-adce-4525-a41c-71cbe2fde2a8">SnmpGetRetry</a>



<a href="https://msdn.microsoft.com/95f7afad-241c-473a-8041-3d1642f9d1fe">SnmpGetTimeout</a>



<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

