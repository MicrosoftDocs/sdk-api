---
UID: NF:winsnmp.SnmpSendMsg
title: SnmpSendMsg function (winsnmp.h)
author: windows-sdk-content
description: A WinSNMP application calls the SnmpSendMsg function to request that the Microsoft WinSNMP implementation transmit an SNMP protocol data unit (PDU), in the form of an SNMP message.
old-location: snmp\snmpsendmsg.htm
tech.root: SNMP
ms.assetid: c4b9f4bb-24f0-4b5e-b12d-8be839b34895
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SnmpSendMsg, SnmpSendMsg function [SNMP], _snmp_snmpsendmsg, snmp.snmpsendmsg, winsnmp/SnmpSendMsg
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
 - SnmpSendMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SnmpSendMsg function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

A WinSNMP application calls the 
<b>SnmpSendMsg</b> function to request that the Microsoft WinSNMP implementation transmit an SNMP protocol data unit (PDU), in the form of an SNMP message. The WinSNMP application specifies a source entity, a destination entity, and a context for the request.

If a WinSNMP application expects a PDU in response to a 
<b>SnmpSendMsg</b> request, it must retrieve the PDU. To do this, the application must call the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function using the session handle returned by 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>.


## -parameters




### -param session [in]

Handle to the WinSNMP session.


### -param srcEntity [in]

Handle to the management entity that initiates the request to send the SNMP message.


### -param dstEntity [in]

Handle to the target entity that will respond to the SNMP request.


### -param context [in]

Handle to the context, (a set of managed object resources), that the target management entity controls.


### -param PDU [in]

Handle to the protocol data unit that contains the SNMP operation request.


## -returns



If the function succeeds, the return value is SNMPAPI_SUCCESS.

If the function fails, the return value is SNMPAPI_FAILURE. To get extended error information, call 
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
The <i>PDU</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SNMPAPI_OPERATION_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The operation specified in the <b>PDU_type</b> field of the PDU is inappropriate for the destination entity. For more information, see the following Remarks section.

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
<b>SnmpSendMsg</b> function executes asynchronously and therefore returns immediately.

The implementation notifies the WinSNMP application when the asynchronous request is completed. The implementation does this by sending a notification message to the window specified by the <i>wMsg</i> and <i>hWnd</i> parameters, respectively, in the initial call to 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a> for the session. When the application window receives the notification message, the WinSNMP application must retrieve the incoming PDU. The application does this by calling the 
<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a> function with the session handle returned by 
<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>.

When a WinSNMP application calls the 
<b>SnmpSendMsg</b> function, the implementation determines which network transport protocol and SNMP version framework to use to complete the transmission request. The implementation determines this by matching its capabilities with properties associated with the requesting session and with the target management entity. This information is available from values in the implementation's database.

If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity uses the SNMP version 1 framework (SNMPv1), the implementation attempts to translate the request to SNMPv1. To do this, the implementation uses the procedures defined in RFC1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework." If translation is not possible, 
<b>SnmpSendMsg</b> fails with the extended error code SNMPAPI_OPERATION_INVALID. This situation occurs, for example, when an application attempts to send a PDU with the <b>SNMP_PDU_InformRequest</b> data type to an SNMPv1 destination entity.

For additional information, see 
<a href="https://msdn.microsoft.com/70c24042-bf44-4484-8e5e-d117e2ba28d5">WinSNMP Programming Tasks</a> and 
<a href="https://msdn.microsoft.com/9ba4b854-fc02-40c1-a92f-7c102c900e95">About SNMP Messages</a>.




## -see-also




<a href="https://msdn.microsoft.com/8d982eb5-a7b5-418e-94ad-3e5dc43d225c">SnmpCreateSession</a>



<a href="https://msdn.microsoft.com/0e306e40-cccc-4083-b3ba-97b8ece0ae35">SnmpRecvMsg</a>



<a href="https://msdn.microsoft.com/ae95ac47-81ff-4715-b3e9-e19c07223712">WinSNMP
		  Functions</a>



<a href="https://msdn.microsoft.com/54d9b61a-815a-41c3-9365-ec4478acc3f2">WinSNMP API Overview</a>
 

 

