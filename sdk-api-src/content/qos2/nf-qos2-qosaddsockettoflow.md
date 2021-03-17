---
UID: NF:qos2.QOSAddSocketToFlow
title: QOSAddSocketToFlow function (qos2.h)
description: Adds a new flow for traffic.
helpviewer_keywords: ["QOSAddSocketToFlow","QOSAddSocketToFlow function [QOS]","QOS_NON_ADAPTIVE_FLOW","qos.qosaddsockettoflow","qos2/QOSAddSocketToFlow"]
old-location: qos\qosaddsockettoflow.htm
tech.root: QOS
ms.assetid: 44136284-b553-446e-a95f-1eac476a7143
ms.date: 12/05/2018
ms.keywords: QOSAddSocketToFlow, QOSAddSocketToFlow function [QOS], QOS_NON_ADAPTIVE_FLOW, qos.qosaddsockettoflow, qos2/QOSAddSocketToFlow
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
 - QOSAddSocketToFlow
 - qos2/QOSAddSocketToFlow
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
 - QOSAddSocketToFlow
---

# QOSAddSocketToFlow function


## -description

The <b>QOSAddSocketToFlow</b> function adds a new flow for traffic.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param Socket [in]

 Identifies the socket that the application will use to flow traffic.

### -param DestAddr [in, optional]

Pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that contains the destination IP address to which the application will send traffic.  The sockaddr structure must specify a destination port.

<div class="alert"><b>Note</b>  <i>DestAddr</i> is optional if the socket is already connected. If this parameter is specified, the remote IP address and port must match those used in the socket's connect call.<p class="note">If the socket is not connected, this parameter must be specified.  If the socket is already connected, this parameter does not need to be specified.  In this case, if the parameter is still specified, the destination host and port must match what was specified during the socket connect call.

<p class="note">Since, under TCP, the socket connect call can be delayed, <b>QOSAddSocketToFlow</b> can be called before a connection is established, passing in the remote system's IP address and port number in the <i>DestAddr</i> parameter.

</div>
<div> </div>

### -param TrafficType [in]

A <a href="/windows/desktop/api/qos2/ne-qos2-qos_traffic_type">QOS_TRAFFIC_TYPE</a> constant that specifies the type of traffic for which this flow will be used.

### -param Flags [in, optional]

Optional flag values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QOS_NON_ADAPTIVE_FLOW"></a><a id="qos_non_adaptive_flow"></a><dl>
<dt><b>QOS_NON_ADAPTIVE_FLOW</b></dt>
</dl>
</td>
<td width="60%">
If specified, the QoS subsystem will not gather data about the network path for this flow.  As a result, functions which rely on bandwidth estimation techniques will not be available.  For example, this would block <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosqueryflow">QOSQueryFlow</a> with an <i>Operation</i> value  of <b>QOSQueryFlowFundamentals</b> and <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosnotifyflow">QOSNotifyFlow</a> with an <i>Operation</i> value of <b>QOSNotifyCongested</b>, <b>QOSNotifyUncongested</b>, and <b>QOSNotifyAvailable</b>. 

</td>
</tr>
</table>

### -param FlowId [in, out]

Pointer to a buffer that receives a flow identifier. On input, this value must be 0.  On output, the buffer contains a flow identifier if the call succeeds.  

If a socket is being added to an existing flow, this parameter will be the identifier of that flow.

An application can make use of this parameter if multiple sockets used can share the same QoS flow properties.  The QoS subsystem, then does not have to incur the overhead of provisioning new flows for subsequent sockets with the same properties.  Note that only non-adaptive flows can have multiple sockets attached to an existing flow.  

A <b>QOS_FLOWID</b> is an unsigned 32-bit integer.

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
<dt><b>ERROR_CONNECTION_REFUSED</b></dt>
</dl>
</td>
<td width="60%">
The remote system refused the network connection.

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

<div class="alert"><b>Note</b>  This value is also returned if a IPv4/v6 mixed address was supplied through the <i>DestAddr</i> parameter.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failed.

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
The request is not supported.

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
</table>

## -remarks

The use of IPv4/v6 mixed addresses is not supported in qWAVE. The address specified by the <i>DestAddr</i> parameter must be either IPv4 or IPv6.

If there is a requirement for network experiments over a specific network interface, the socket must be bound to that particular interface. Otherwise the most appropriate interface for the experiment, as indicated by the network stack, is assigned by the qWAVE subsystem.

Network traffic associated with this flow is not affected by making this call alone.  For example, packet prioritization does not occur immediately.

There are two categories of applications that use this function:  adaptive and non-adaptive.  An adaptive application makes use of notifications and information in the <a href="/windows/desktop/api/qos2/ns-qos2-qos_flow_fundamentals">QOS_FLOW_FUNDAMENTALS</a> structure for adapting to network changes such as congestion.  The qWAVE service uses Link Layer Topology Discovery (LLTD) QoS extensions for adaptive flows which can be present on the destination device.

After calling this function adaptive A/V applications should call the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a> function with an <i>Operation</i> value of <b>QOSSetFlowRate</b> to affect network traffic.

A non-adaptive application either does not adapt to changing network characteristics or is sending traffic to an endpoint that does not support adaptive capabilities as indicated by ERROR_NOT_SUPPORTED.

Non-adaptive applications, or adaptive applications making non-adaptive flows, should call this function with the <b>QOS_NON_ADAPTIVE_FLOW</b> flag.  After calling this function A/V applications should call the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a> function with a <i>Operation</i>. <b>QOSSetFlow</b> does not need to be called unless shaping is desired.


#### Examples

The following code illustrates  the use of <b>QOSAddSocketFromFlow</b>. The  <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> function is also shown to provide information on initialization of parameters used by <b>QOSAddSocketFromFlow</b>.

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

The Winsock2.h header file must be included to use WSAGetLastError and other Winsock functions.


```cpp
QOS_VERSION    Version;
HANDLE         QoSHandle = NULL;
QOS_FLOWID     QoSFlowId = 0; // Flow Id must be 0.
SOCKET        ConnectionSocket;
BOOL          QoSResult;


// Initialize the QoS version parameter.
Version.MajorVersion = 1;
Version.MinorVersion = 0;

// Get a handle to the QoS subsystem.
QoSResult = QOSCreateHandle(
    &Version, 
    &QoSHandle );

if (QoSResult != TRUE)
{
    std::cerr << "QOSCreateHandle failed. Error: "; 
    std::cerr << WSAGetLastError() << std::endl;
}

// Initialization of ConnectionSocket   
// omitted for brevity, but is needed.
/////////////////////////////////////
 
// Add socket to flow.
QoSResult = QOSAddSocketToFlow(
    QoSHandle,
    ConnectionSocket,
    NULL,
    QOSTrafficTypeExcellentEffort, 
     QOS_NON_ADAPTIVE_FLOW, 
    &QoSFlowId);

if (QoSResult != TRUE)
{
    std::cerr << "QOSAddSocketToFlow failed. Error: "; 
    std::cerr << WSAGetLastError() << std::endl;
}


```

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>