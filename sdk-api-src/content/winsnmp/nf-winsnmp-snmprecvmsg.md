---
UID: NF:winsnmp.SnmpRecvMsg
title: SnmpRecvMsg function
author: windows-driver-content
description: The WinSNMP SnmpRecvMsg function retrieves the results of a completed asynchronous request submitted by a call to the SnmpSendMsg function, in the form of an SNMP message.
old-location: snmp\snmprecvmsg.htm
old-project: SNMP
ms.assetid: 0e306e40-cccc-4083-b3ba-97b8ece0ae35
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SnmpRecvMsg, SnmpRecvMsg function [SNMP], _snmp_snmprecvmsg, snmp.snmprecvmsg, winsnmp/SnmpRecvMsg
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
-	SnmpRecvMsg
product: Windows
targetos: Windows
req.lib: Wsnmp32.lib
req.dll: Wsnmp32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SnmpRecvMsg function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpRecvMsg</b> function retrieves the results of a completed asynchronous request submitted by a call to the 
<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a> function, in the form of an SNMP message. The 
<b>SnmpRecvMsg</b> function also returns outstanding trap data and notifications registered for a WinSNMP session.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param srcEntity [out]

Pointer to a variable that receives a handle to the entity that sends the message. Note that the <i>srcEntity</i> parameter to the 
<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a> function specifies a handle to the management entity that registers for trap notification.


### -param dstEntity [out]

Pointer to a variable that receives a handle to the entity that receives the message. Note that the <i>dstEntity</i> parameter to the 
<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a> function specifies a handle to the management entity that sends traps.


### -param context [out]

Pointer to a variable that receives a handle to the context, which is a set of managed object resources. The entity specified by the <i>srcEntity</i> parameter issues the message from this context.


### -param PDU [out]

Pointer to a variable that receives a handle to the protocol data unit (PDU) component of the message.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS, and the output parameters contain the values indicated in the preceding parameter descriptions.

If the function fails, the return value is SNMPAPI_FAILURE. If the function fails with an extended error code that indicates a network transport layer error, that is, one that begins with SNMPAPI_TL_, the output parameters also contain the values indicated preceding to enable the WinSNMP application to recover gracefully.

To get extended error information, call 
<a href="https://msdn.microsoft.com/0cfb2bc3-cfa5-4806-9dcf-119541463e7b">SnmpGetLastError</a>. The 
<b>SnmpGetLastError</b> function may return one of the following WinSNMP or network transport layer errors.

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
<dt><b>SNMPAPI_NOOP</b></dt>
</dl>
</td>
<td width="60%">
The specified session has no messages in its queue at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The network transport layer was not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The network transport layer does not support the SNMP protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The network subsystem failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_RESOURCE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A resource error occurred in the network transport layer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_UNDELIVERABLE</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>dstEntity</i> parameter is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_SRC_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The entity specified by the <i>srcEntity</i> parameter was not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_INVALID_PARAM</b></dt>
</dl>
</td>
<td width="60%">
A network transport layer function call received an invalid input parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_PDU_TOO_BIG</b></dt>
</dl>
</td>
<td width="60%">
The PDU is too large for the network transport layer to send or receive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_TL_OTHER</b></dt>
</dl>
</td>
<td width="60%">
An undefined network transport layer error occurred.

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
 

For additional information, see 
<a href="https://msdn.microsoft.com/2ff535b1-76cb-42aa-baeb-14c1a1bc41ce">Network Transport Errors</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> function passes an application window handle and notification message identifier to the Microsoft WinSNMP implementation. When the application window receives the notification message specified by the <i>wMsg</i> parameter, the WinSNMP application must call the 
<b>SnmpRecvMsg</b> function with the session handle returned by 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> to retrieve an incoming protocol data unit (PDU). For additional information, see 
<a href="https://msdn.microsoft.com/9ba4b854-fc02-40c1-a92f-7c102c900e95">About SNMP Messages</a>.

The 
<b>SnmpRecvMsg</b> function instantiates four objects and allocates their resources: two entity handles, a context handle, and a PDU handle. The handle to the variable bindings list component of the returned PDU is not instantiated until the WinSNMP application calls the 
<a href="https://msdn.microsoft.com/5dff1bc0-aac4-490f-aef0-11d090567761">SnmpGetPduData</a> function. When it no longer needs the resources 
<b>SnmpRecvMsg</b> returns, the WinSNMP application must free the individual resources using the WinSNMP function that corresponds to the resource. For additional information, see 
<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>, 
<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>, and 
<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>.

When the implementation receives traps from an entity operating under the SNMP version 1 framework (SNMPv1), it translates the traps to the SNMP version 2C (SNMPv2C) format. Therefore, when 
<b>SnmpRecvMsg</b> delivers a trap it is always in the SNMPv2C format. For additional information, see 
<a href="https://msdn.microsoft.com/472f67ba-05d5-46f7-a2f1-1cef6182574e">Translating Traps from SNMPv1 to SNMPv2C</a> and 
<a href="https://msdn.microsoft.com/70c24042-bf44-4484-8e5e-d117e2ba28d5">WinSNMP Programming Tasks</a>.




## -see-also




<a href="https://msdn.microsoft.com/15ab137e-86ea-43fc-ac8c-cd6a76feaa04">SnmpFreeContext</a>



<a href="https://msdn.microsoft.com/82f331e8-1768-470f-b924-16262e06f099">SnmpFreeEntity</a>



<a href="https://msdn.microsoft.com/243e52aa-2b05-4c41-9f89-cf9c66517da6">SnmpFreePdu</a>



<a href="https://msdn.microsoft.com/5dff1bc0-aac4-490f-aef0-11d090567761">SnmpGetPduData</a>



<a href="https://msdn.microsoft.com/ea2476b4-2f98-4295-95c4-c96c6b719e05">SnmpRegister</a>



<a href="https://msdn.microsoft.com/c4b9f4bb-24f0-4b5e-b12d-8be839b34895">SnmpSendMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

