---
UID: NF:winsnmp.SnmpDecodeMsg
title: SnmpDecodeMsg function
author: windows-sdk-content
description: The WinSNMP SnmpDecodeMsg function decodes an encoded SNMP message into its components. This function performs the opposite action of the WinSNMP SnmpEncodeMsg function.
old-location: snmp\snmpdecodemsg.htm
tech.root: SNMP
ms.assetid: d19d6451-1640-4c3b-9e60-d9cb591cf173
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SnmpDecodeMsg, SnmpDecodeMsg function [SNMP], _snmp_snmpdecodemsg, snmp.snmpdecodemsg, winsnmp/SnmpDecodeMsg
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
 - SnmpDecodeMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpDecodeMsg function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpDecodeMsg</b> function decodes an encoded SNMP message into its components. This function performs the opposite action of the WinSNMP 
<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a> function.


## -parameters




### -param session [in]

Handle to the WinSNMP session. This parameter is required. For additional information, see the following Remarks section.


### -param srcEntity [out]

Pointer to a variable that receives a handle to the source management entity. For more information, see the following Remarks section.


### -param dstEntity [out]

Pointer to a variable that receives a handle to the target management entity. For more information, see the following Remarks section.


### -param context [out]

Pointer to a variable that receives a handle to the context (a set of managed object resources) that the target management entity controls.


### -param pdu [out]

Pointer to a variable that receives a handle to the SNMP protocol data unit (PDU).


### -param msgBufDesc [in]

Pointer to an 
<a href="https://msdn.microsoft.com/en-us/library/Aa377995(v=VS.85).aspx">smiOCTETS</a> structure that contains the SNMP message to decode into its components. The <b>len</b> member of the structure specifies the maximum number of bytes to process; the <b>ptr</b> member points to the encoded SNMP message.


## -returns



If the function succeeds, the return value is the number of decoded bytes. This value can be equal to, or less than, the <b>len</b> member of the 
<a href="https://msdn.microsoft.com/en-us/library/Aa377995(v=VS.85).aspx">smiOCTETS</a> structure pointed to by the <i>msgBufDesc</i> parameter.

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
<dt><b>SNMPAPI_OUTPUT_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The output buffer length is insufficient. No output parameters were created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_MESSAGE_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The SNMP message format in the buffer indicated by the <i>msgBufDesc</i> parameter is invalid. No output parameters were created.

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



The Microsoft WinSNMP implementation returns a value of zero in the <i>srcEntity</i> and the <i>dstEntity</i> parameters when an application submits an SNMPv1 or an SNMPv2C message to the 
<b>SnmpDecodeMsg</b> function. This is because the message format does not include the address information necessary to create WinSNMP entity resources.

The Microsoft WinSNMP implementation allocates resources to the WinSNMP application as a result of a successful call to the 
<b>SnmpDecodeMsg</b> function. It is recommended that the WinSNMP application free individual resources with the WinSNMP function that corresponds to the resource. For additional information, see 
<a href="https://msdn.microsoft.com/3e4cbbc5-18bc-4731-971c-6e533d904f56">Freeing WinSNMP Descriptors</a> and 
<a href="https://msdn.microsoft.com/52e911f3-9b28-4ac3-a080-44fb18f5633e">WinSNMP Data Management Concepts</a>.




## -see-also




<a href="https://msdn.microsoft.com/0c8ebf49-b59e-4483-a7cf-456794e24bd6">SnmpEncodeMsg</a>



<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>



<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>



<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377995(v=VS.85).aspx">smiOCTETS</a>
 

 

