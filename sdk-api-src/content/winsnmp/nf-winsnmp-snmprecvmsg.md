---
UID: NF:winsnmp.SnmpRecvMsg
title: SnmpRecvMsg function (winsnmp.h)
description: The WinSNMP SnmpRecvMsg function retrieves the results of a completed asynchronous request submitted by a call to the SnmpSendMsg function, in the form of an SNMP message.
helpviewer_keywords: ["SnmpRecvMsg","SnmpRecvMsg function [SNMP]","_snmp_snmprecvmsg","snmp.snmprecvmsg","winsnmp/SnmpRecvMsg"]
old-location: snmp\snmprecvmsg.htm
tech.root: SNMP
ms.assetid: 0e306e40-cccc-4083-b3ba-97b8ece0ae35
ms.date: 12/05/2018
ms.keywords: SnmpRecvMsg, SnmpRecvMsg function [SNMP], _snmp_snmprecvmsg, snmp.snmprecvmsg, winsnmp/SnmpRecvMsg
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SnmpRecvMsg
 - winsnmp/SnmpRecvMsg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsnmp32.dll
api_name:
 - SnmpRecvMsg
---

# SnmpRecvMsg function


## -description

<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The WinSNMP 
<b>SnmpRecvMsg</b> function retrieves the results of a completed asynchronous request submitted by a call to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a> function, in the form of an SNMP message. The 
<b>SnmpRecvMsg</b> function also returns outstanding trap data and notifications registered for a WinSNMP session.

## -parameters

### -param session [in]

Handle to the WinSNMP session.

### -param srcEntity [out]

Pointer to a variable that receives a handle to the entity that sends the message. Note that the <i>srcEntity</i> parameter to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a> function specifies a handle to the management entity that registers for trap notification.

### -param dstEntity [out]

Pointer to a variable that receives a handle to the entity that receives the message. Note that the <i>dstEntity</i> parameter to the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a> function specifies a handle to the management entity that sends traps.

### -param context [out]

Pointer to a variable that receives a handle to the context, which is a set of managed object resources. The entity specified by the <i>srcEntity</i> parameter issues the message from this context.

### -param PDU [out]

Pointer to a variable that receives a handle to the protocol data unit (PDU) component of the message.

## -returns

If the function succeeds, the return value is SNMPAPI_SUCCESS, and the output parameters contain the values indicated in the preceding parameter descriptions.

If the function fails, the return value is SNMPAPI_FAILURE. If the function fails with an extended error code that indicates a network transport layer error, that is, one that begins with SNMPAPI_TL_, the output parameters also contain the values indicated preceding to enable the WinSNMP application to recover gracefully.

To get extended error information, call 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetlasterror">SnmpGetLastError</a>. The 
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
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpstartup">SnmpStartup</a> function did not complete successfully.

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
<a href="/windows/desktop/SNMP/network-transport-errors">Network Transport Errors</a>.

## -remarks

The 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> function passes an application window handle and notification message identifier to the Microsoft WinSNMP implementation. When the application window receives the notification message specified by the <i>wMsg</i> parameter, the WinSNMP application must call the 
<b>SnmpRecvMsg</b> function with the session handle returned by 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpcreatesession">SnmpCreateSession</a> to retrieve an incoming protocol data unit (PDU). For additional information, see 
<a href="/windows/desktop/SNMP/about-snmp-messages">About SNMP Messages</a>.

The 
<b>SnmpRecvMsg</b> function instantiates four objects and allocates their resources: two entity handles, a context handle, and a PDU handle. The handle to the variable bindings list component of the returned PDU is not instantiated until the WinSNMP application calls the 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetpdudata">SnmpGetPduData</a> function. When it no longer needs the resources 
<b>SnmpRecvMsg</b> returns, the WinSNMP application must free the individual resources using the WinSNMP function that corresponds to the resource. For additional information, see 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>, 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>, and 
<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>.

When the implementation receives traps from an entity operating under the SNMP version 1 framework (SNMPv1), it translates the traps to the SNMP version 2C (SNMPv2C) format. Therefore, when 
<b>SnmpRecvMsg</b> delivers a trap it is always in the SNMPv2C format. For additional information, see 
<a href="/windows/desktop/SNMP/translating-traps-from-snmpv1-to-snmpv2c">Translating Traps from SNMPv1 to SNMPv2C</a> and 
<a href="/windows/desktop/SNMP/winsnmp-programming-tasks">WinSNMP Programming Tasks</a>.

## -see-also

<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreecontext">SnmpFreeContext</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreeentity">SnmpFreeEntity</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpfreepdu">SnmpFreePdu</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpgetpdudata">SnmpGetPduData</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpregister">SnmpRegister</a>



<a href="/windows/desktop/api/winsnmp/nf-winsnmp-snmpsendmsg">SnmpSendMsg</a>



<a href="/windows/desktop/SNMP/winsnmp-functions">WinSNMP
		  Functions</a>



<a href="/windows/desktop/SNMP/winsnmp-api">WinSNMP API Overview</a>