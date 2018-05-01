---
UID: NF:winsnmp.SnmpDuplicatePdu
title: SnmpDuplicatePdu function
author: windows-driver-content
description: The WinSNMP SnmpDuplicatePdu function duplicates the SNMP protocol data unit (PDU) that the PDU parameter identifies, allocating any necessary memory for the duplicate PDU.
old-location: snmp\snmpduplicatepdu.htm
old-project: SNMP
ms.assetid: 4507cc9b-36a5-45bf-916d-9dc82ac381a5
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpDuplicatePdu, SnmpDuplicatePdu function [SNMP], _snmp_snmpduplicatepdu, snmp.snmpduplicatepdu, winsnmp/SnmpDuplicatePdu
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wsnmp32.dll
api_name:
-	SnmpDuplicatePdu
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpDuplicatePdu function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDuplicatePdu</b> function duplicates the SNMP protocol data unit (PDU) that the <i>PDU</i> parameter identifies, allocating any necessary memory for the duplicate PDU.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param PDU [in]

Handle to the PDU to duplicate. The 
<b>SnmpDuplicatePdu</b> function provides a unique handle to each PDU within the calling application.


## -returns



If the function succeeds, the return value is a handle that identifies the new duplicate PDU.

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
<dt><b>SNMPAPI_SESSION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The session handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The PDU handle is invalid.

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



To release resources allocated by the 
<b>SnmpDuplicatePdu</b> function for a new PDU, a WinSNMP application must call the 
<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a> function.




## -see-also




<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>



<a href="https://msdn.microsoft.com/5dff1bc0-aac4-490f-aef0-11d090567761">SnmpGetPduData</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

