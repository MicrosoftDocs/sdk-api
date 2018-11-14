---
UID: NF:winsnmp.SnmpEncodeMsg
title: SnmpEncodeMsg function
author: windows-sdk-content
description: The Microsoft WinSNMP implementation uses the parameters passed in the WinSNMP SnmpEncodeMsg function to encode an SNMP message.
old-location: snmp\snmpencodemsg.htm
tech.root: SNMP
ms.assetid: 0c8ebf49-b59e-4483-a7cf-456794e24bd6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SnmpEncodeMsg, SnmpEncodeMsg function [SNMP], _snmp_snmpencodemsg, snmp.snmpencodemsg, winsnmp/SnmpEncodeMsg
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
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpEncodeMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SnmpEncodeMsg
: 
---

# SnmpEncodeMsg function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The Microsoft WinSNMP implementation uses the parameters passed in the WinSNMP 
<b>SnmpEncodeMsg</b> function to encode an SNMP message. The implementation returns the encoded SNMP message to the WinSNMP application in the buffer specified by the <i>msgBufDesc</i> parameter.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param srcEntity [in]

Handle to the management entity that initiates the request to encode the SNMP message.


### -param dstEntity [in]

Handle to the target management entity.


### -param context [in]

Handle to the context (a set of managed object resources) that the target management entity controls.


### -param pdu [in]

Handle to the PDU that contains the SNMP operation request.


### -param msgBufDesc [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure that receives the encoded SNMP message.


## -returns



If the function succeeds, the return value is the length, in bytes, of the encoded SNMP message. This number is also the value of the <b>len</b> member of the 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure pointed to by the <i>msgBufDesc</i> parameter.

If the function fails, the return value is SNMPAPI_FAILURE. For additional information, see the following Remarks section. To get extended error information, call 
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
The <i>session</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_ENTITY_INVALID</b></dt>
</dl>
</td>
<td width="60%">
One or both of the entity parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_CONTEXT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>context</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_PDU_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdu</i> parameter is invalid.

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



The first five parameters passed to the 
<b>SnmpEncodeMsg</b> function are the same parameters that are passed to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function.

The WinSNMP application must call the 
<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a> function to free resources allocated for the <b>ptr</b> member of the 
<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a> structure. This is the structure pointed to by the <i>msgBufDesc</i> parameter. For additional information, see 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.

On input, the 
<b>SnmpEncodeMsg</b> function ignores the members of the structure pointed to by the <i>msgBufDesc</i> parameter. The implementation overwrites the members of the structure if the function completes successfully.

The implementation verifies the format of the first five input parameters. If one of the parameters is invalid, 
<b>SnmpEncodeMsg</b> returns SNMPAPI_FAILURE, and 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a> returns an extended error code.




## -see-also




<a href="https://msdn.microsoft.com/d19d6451-1640-4c3b-9e60-d9cb591cf173">SnmpDecodeMsg</a>



<a href="https://msdn.microsoft.com/535f728d-6964-47b6-9913-7cd38356053d">SnmpFreeDescriptor</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/d53da0e8-ce7d-4923-90c3-2469cbd9d9b1">smiOCTETS</a>
 

 

