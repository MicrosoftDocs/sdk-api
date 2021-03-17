---
UID: NF:qos2.QOSNotifyFlow
title: QOSNotifyFlow function (qos2.h)
description: Registers the calling application to receive a notification.
helpviewer_keywords: ["QOSNotifyFlow","QOSNotifyFlow function [QOS]","qos.qosnotifyflow","qos2/QOSNotifyFlow"]
old-location: qos\qosnotifyflow.htm
tech.root: QOS
ms.assetid: e6d541fe-2aeb-4969-b138-869754dbdaa3
ms.date: 12/05/2018
ms.keywords: QOSNotifyFlow, QOSNotifyFlow function [QOS], qos.qosnotifyflow, qos2/QOSNotifyFlow
req.header: qos2.h
req.include-header: Qos2.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QOSNotifyFlow
 - qos2/QOSNotifyFlow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - qwave.dll
api_name:
 - QOSNotifyFlow
---

# QOSNotifyFlow function


## -description

The <b>QOSNotifyFlow</b> function registers the calling application to receive a notification about changes in network characteristics, such as congestion. Notifications may also be sent when a desired throughput is able to be achieved.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param FlowId [in]

Specifies the flow identifier from which the application wishes to receive notifications. A <b>QOS_FLOWID</b> is an unsigned 32-bit integer.

### -param Operation [in]

A <a href="/windows/desktop/api/qos2/ne-qos2-qos_notify_flow">QOS_NOTIFY_FLOW</a> value that indicates what the type of  notification being requested.

### -param Size [in, out, optional]

Indicates the size of the <i>Buffer</i> parameter, in bytes.

On function return, if successful, this parameter will specify the number of bytes copied into <i>Buffer</i>.

If this call fails with <b>ERROR_INSUFFICIENT_BUFFER</b>, this parameter will indicate the minimum required <i>Buffer</i> size in order to successfully complete this operation.

### -param Buffer [in, out]

Pointer to a UINT64 that indicates the bandwidth at which point a notification will be sent.  This parameter is only used if the <i>Operation</i> parameter is set to <b>QOSNotifyAvailable</b>. For the <b>QOSNotifyCongested</b> and <b>QOSNotifyUncongested</b> options, this parameter must be set to <b>NULL</b> on input.

### -param Flags

Reserved for future use.  This parameter must be set to 0.

### -param Overlapped [out, optional]

Pointer to an OVERLAPPED structure used for asynchronous output. This must be se to <b>NULL</b> if this function is not being called asynchronously.

## -returns

If the function succeeds, a return value of nonzero is sent when the conditions set by the <i>Operation</i> parameter are met.

If the function fails, the return value is 0.  To get extended error information, call <b>GetLastError</b>.  Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DISABLED_BY_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The QoS subsystem is currently configured by policy to not allow this operation on the network path between this host and the destination host.  For example, the default policy prevents qWAVE experiments from running to off-link destinations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that notification request was successfully received.  Results will be returned during overlapped completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>QOSHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FlowId</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid <i>FlowId</i> specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation being performed requires information that the QoS subsystem does not have.  Obtaining this information on this network is currently not supported.  For example, bandwidth estimations cannot be obtained on a network path where the destination host is off-link.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are insufficient resources to carry out the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The request could not be performed because of an I/O device error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_REINITIALIZATION_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The QOS subsystem has determined that the operation requested could not be completed on the network path specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ADAP_HDW_ERR</b></dt>
</dl>
</td>
<td width="60%">
A network adapter hardware error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HOST_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The network location cannot be reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNEXP_NET_ERR</b></dt>
</dl>
</td>
<td width="60%">
The network connection with the remote host failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
There is already a request for notifications of the same type pending on this flow.

</td>
</tr>
</table>

## -remarks

This function may be called asynchronously.

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>