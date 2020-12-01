---
UID: NF:qos2.QOSQueryFlow
title: QOSQueryFlow function (qos2.h)
description: Requests information about a specific flow.
helpviewer_keywords: ["QOSQueryFlow","QOSQueryFlow function [QOS]","QOSQueryFlowFundamentals","QOSQueryOutgoingRate","QOSQueryPacketPriority","QOS_QUERYFLOW_FRESH","qos.qosqueryflow","qos2/QOSQueryFlow"]
old-location: qos\qosqueryflow.htm
tech.root: QOS
ms.assetid: 8cae3ba2-beca-45e2-9526-2d917abc2606
ms.date: 12/05/2018
ms.keywords: QOSQueryFlow, QOSQueryFlow function [QOS], QOSQueryFlowFundamentals, QOSQueryOutgoingRate, QOSQueryPacketPriority, QOS_QUERYFLOW_FRESH, qos.qosqueryflow, qos2/QOSQueryFlow
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
 - QOSQueryFlow
 - qos2/QOSQueryFlow
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
 - QOSQueryFlow
---

# QOSQueryFlow function


## -description

The <b>QOSQueryFlow</b> function requests information about a specific flow added to the QoS subsystem. This function may be called asynchronously.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param FlowId [in]

Specifies a flow identifier. A <b>QOS_FLOWID</b> is an unsigned 32-bit integer.

### -param Operation [in]

Specifies which type of flow information is being queried. This parameter specifies what structure the <i>Buffer</i> will contain.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QOSQueryFlowFundamentals"></a><a id="qosqueryflowfundamentals"></a><a id="QOSQUERYFLOWFUNDAMENTALS"></a><dl>
<dt><b>QOSQueryFlowFundamentals</b></dt>
</dl>
</td>
<td width="60%">
<i>Buffer</i> will contain a <a href="/windows/desktop/api/qos2/ns-qos2-qos_flow_fundamentals">QOS_FLOW_FUNDAMENTALS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="QOSQueryPacketPriority"></a><a id="qosquerypacketpriority"></a><a id="QOSQUERYPACKETPRIORITY"></a><dl>
<dt><b>QOSQueryPacketPriority</b></dt>
</dl>
</td>
<td width="60%">
<i>Buffer</i> will contain a <a href="/windows/desktop/api/qos2/ns-qos2-qos_packet_priority">QOS_PACKET_PRIORITY</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="QOSQueryOutgoingRate"></a><a id="qosqueryoutgoingrate"></a><a id="QOSQUERYOUTGOINGRATE"></a><dl>
<dt><b>QOSQueryOutgoingRate</b></dt>
</dl>
</td>
<td width="60%">
<i>Buffer</i> will contain a <b>UINT64</b> value that indicates the flow rate specified when requesting the contract, in bits per second.

</td>
</tr>
</table>

### -param Size [in, out]

Indicates the size of the <i>Buffer</i> parameter, in bytes.

On function return, if successful, this parameter will specify the number of bytes copied into <i>Buffer</i>.

If this call fails with <b>ERROR_INSUFFICIENT_BUFFER</b>, this parameter will indicate the minimum required <i>Buffer</i> size in order to successfully complete this operation.

### -param Buffer [out]

Pointer to the structure specified by the value of the <i>Operation</i> parameter.

### -param Flags [in, optional]

Flags pertaining to the data being returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QOS_QUERYFLOW_FRESH"></a><a id="qos_queryflow_fresh"></a><dl>
<dt><b>QOS_QUERYFLOW_FRESH</b></dt>
</dl>
</td>
<td width="60%">
The QOS subsystem will only return fresh, not cached,  data.  If fresh data is unavailable, it will try to obtain such data, at the expense of possibly taking more time.  If this is not possible, the call will fail with the error code <b>ERROR_RETRY</b>.

This flag is only applicable when the <i>Operation</i> parameter is set to <b>QOSQueryFlowFundamentals</b>.

</td>
</tr>
</table>

### -param Overlapped [out, optional]

Pointer to an OVERLAPPED structure used for asynchronous output. This must be set to <b>NULL</b> if this function is not being called asynchronously.

## -returns

If the function succeeds, the return value is nonzero.

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
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The request to the QOS subsystem timed out before enough useful information could be gathered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer length as specified by the <b>Size</b> parameter is not sufficient for the queried data.  The <b>Size</b> parameter now contains the minimum required size.

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
The <i>FlowId</i> parameter or <i>Buffer</i> size is insufficient.

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
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the update flow request was successfully initiated.

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
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The is no valid data to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RETRY</b></dt>
</dl>
</td>
<td width="60%">
There is currently insufficient data about networking conditions to answer the query.  This is typically a transient state where qWAVE has erred on the side of caution as it awaits more data before ascertaining the state of the network.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>