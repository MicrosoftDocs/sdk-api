---
UID: NF:qos2.QOSAddSocketToFlow
title: QOSAddSocketToFlow function
author: windows-driver-content
description: Adds a new flow for traffic.
old-location: qos\qosaddsockettoflow.htm
old-project: QOS
ms.assetid: 44136284-b553-446e-a95f-1eac476a7143
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: QOSAddSocketToFlow, QOSAddSocketToFlow function [QOS], QOS_NON_ADAPTIVE_FLOW, qos.qosaddsockettoflow, qos2/QOSAddSocketToFlow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: QOS_TRAFFIC_TYPE, *PQOS_TRAFFIC_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	qwave.dll
api_name:
-	QOSAddSocketToFlow
product: Windows
targetos: Windows
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# QOSAddSocketToFlow function


## -description


The <b>QOSAddSocketToFlow</b> function adds a new flow for traffic.


## -parameters




### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>.


### -param Socket [in]

 Identifies the socket that the application will use to flow traffic.


### -param DestAddr [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure that contains the destination IP address to which the application will send traffic.  The sockaddr structure must specify a destination port.

<div class="alert"><b>Note</b>  <i>DestAddr</i> is optional if the socket is already connected. If this parameter is specified, the remote IP address and port must match those used in the socket's connect call.<p class="note">If the socket is not connected, this parameter must be specified.  If the socket is already connected, this parameter does not need to be specified.  In this case, if the parameter is still specified, the destination host and port must match what was specified during the socket connect call.

<p class="note">Since, under TCP, the socket connect call can be delayed, <b>QOSAddSocketToFlow</b> can be called before a connection is established, passing in the remote system's IP address and port number in the <i>DestAddr</i> parameter.

</div>
<div> </div>

### -param TrafficType [in]

A <a href="https://msdn.microsoft.com/89145c7f-0b67-4eff-b462-049b047e6602">QOS_TRAFFIC_TYPE</a> constant that specifies the type of traffic for which this flow will be used.


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
If specified, the QoS subsystem will not gather data about the network path for this flow.  As a result, functions which rely on bandwidth estimation techniques will not be available.  For example, this would block <a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a> with an <i>Operation</i> value  of <b>QOSQueryFlowFundamentals</b> and <a href="https://msdn.microsoft.com/e6d541fe-2aeb-4969-b138-869754dbdaa3">QOSNotifyFlow</a> with an <i>Operation</i> value of <b>QOSNotifyCongested</b>, <b>QOSNotifyUncongested</b>, and <b>QOSNotifyAvailable</b>. 

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
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> again.

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

There are two categories of applications that use this function:  adaptive and non-adaptive.  An adaptive application makes use of notifications and information in the <a href="https://msdn.microsoft.com/3e6cbd5b-8bd3-4f08-9192-35604db5dc3a">QOS_FLOW_FUNDAMENTALS</a> structure for adapting to network changes such as congestion.  The qWAVE service uses Link Layer Topology Discovery (LLTD) QoS extensions for adaptive flows which can be present on the destination device.

After calling this function adaptive A/V applications should call the <a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a> function with an <i>Operation</i> value of <b>QOSSetFlowRate</b> to affect network traffic.

A non-adaptive application either does not adapt to changing network characteristics or is sending traffic to an endpoint that does not support adaptive capabilities as indicated by ERROR_NOT_SUPPORTED.

Non-adaptive applications, or adaptive applications making non-adaptive flows, should call this function with the <b>QOS_NON_ADAPTIVE_FLOW</b> flag.  After calling this function A/V applications should call the <a href="https://msdn.microsoft.com/b30e8887-4445-480d-aba8-79ec36384648">QOSSetFlow</a> function with a <i>Operation</i>. <b>QOSSetFlow</b> does not need to be called unless shaping is desired.


#### Examples

The following code illustrates  the use of <b>QOSAddSocketFromFlow</b>. The  <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> function is also shown to provide information on initialization of parameters used by <b>QOSAddSocketFromFlow</b>.

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

The Winsock2.h header file must be included to use WSAGetLastError and other Winsock functions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>QOS_VERSION    Version;
HANDLE         QoSHandle = NULL;
QOS_FLOWID     QoSFlowId = 0; // Flow Id must be 0.
SOCKET        ConnectionSocket;
BOOL          QoSResult;


// Initialize the QoS version parameter.
Version.MajorVersion = 1;
Version.MinorVersion = 0;

// Get a handle to the QoS subsystem.
QoSResult = QOSCreateHandle(
    &amp;Version, 
    &amp;QoSHandle );

if (QoSResult != TRUE)
{
    std::cerr &lt;&lt; "QOSCreateHandle failed. Error: "; 
    std::cerr &lt;&lt; WSAGetLastError() &lt;&lt; std::endl;
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
    &amp;QoSFlowId);

if (QoSResult != TRUE)
{
    std::cerr &lt;&lt; "QOSAddSocketToFlow failed. Error: "; 
    std::cerr &lt;&lt; WSAGetLastError() &lt;&lt; std::endl;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>



<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

