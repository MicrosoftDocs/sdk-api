---
UID: NF:qos2.QOSSetFlow
title: QOSSetFlow function
author: windows-sdk-content
description: Is called by an application to request the QOS subsystem to prioritize the application's packets and change the flow traffic.
old-location: qos\qossetoutgoingrate.htm
tech.root: QOS
ms.assetid: b30e8887-4445-480d-aba8-79ec36384648
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: QOSSetFlow, QOSSetFlow function [QOS], QOSSetOutgoingDSCPValue, QOSSetOutgoingRate, QOSSetTrafficType, qos.qossetoutgoingrate, qos2/QOSSetFlow
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
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - qwave.dll
api_name:
 - QOSSetFlow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- QOSSetFlow
: 
---

# QOSSetFlow function


## -description


The <b>QOSSetFlow</b> function is called by an application to request the QOS subsystem to prioritize the application's packets and change the flow traffic.  This function is also used to notify the QoS subsystem of a flow change: for example, if the flow rate is changed in order to account for network congestion, or if the QoS priority value requires adjustment for transferring or streaming different types of content over a single persistent socket connection.


## -parameters




### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>.


### -param FlowId [in]

A flow identifier. A <b>QOS_FLOWID</b> is an unsigned 32-bit integer.


### -param Operation [in]

A <a href="https://msdn.microsoft.com/986652bc-df2f-4210-bf9c-1a5d8c3ee773">QOS_SET_FLOW</a> enumerated type that identifies what will be changed in the flow.  This parameter specifies what structure the <i>Buffer</i> will contain.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QOSSetTrafficType"></a><a id="qossettraffictype"></a><a id="QOSSETTRAFFICTYPE"></a><dl>
<dt><b>QOSSetTrafficType</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The traffic type of the flow will be changed.  The <i>Buffer</i> will contain a pointer to a <a href="https://msdn.microsoft.com/89145c7f-0b67-4eff-b462-049b047e6602">QOS_TRAFFIC_TYPE</a> constant.

</td>
</tr>
<tr>
<td width="40%"><a id="QOSSetOutgoingRate"></a><a id="qossetoutgoingrate"></a><a id="QOSSETOUTGOINGRATE"></a><dl>
<dt><b>QOSSetOutgoingRate</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The flow rate will be changed. The <i>Buffer</i> will contain a pointer to a <a href="https://msdn.microsoft.com/6f0408fa-842c-4c6c-954b-cdc8a77b4bd3">QOS_FLOWRATE_OUTGOING</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="QOSSetOutgoingDSCPValue"></a><a id="qossetoutgoingdscpvalue"></a><a id="QOSSETOUTGOINGDSCPVALUE"></a><dl>
<dt><b>QOSSetOutgoingDSCPValue</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Windows 7, Windows Server 2008 R2, and later: The outgoing DSCP value will be changed. The <i>Buffer</i> will contain a pointer to a <b>DWORD</b> value that defines the arbitrary DSCP value.

<div class="alert"><b>Note</b>  This setting requires the calling application be a member of the Administrators or the  Network Configuration Operators group.</div>
<div> </div>
</td>
</tr>
</table>
 


### -param Size [in]

The size of the <i>Buffer</i> parameter, in bytes.


### -param Buffer [in]

Pointer to the structure specified by the value of the <i>Operation</i> parameter.


### -param Flags

Reserved for future use. This parameter must be set to 0.


### -param Overlapped [out, optional]

Pointer to an OVERLAPPED structure used for asynchronous output.  This must be set to <b>NULL</b> if this function is not being called asynchronously.


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
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The update flow request was successfully received.  Results will be returned during overlapped completion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges for the requested operation.

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
<dt><b>ERROR_NETWORK_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The requested flow properties were not available on this path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>FlowId</i> parameter specified cannot be found.

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
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> again.

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
<dt><b>ERROR_RETRY</b></dt>
</dl>
</td>
<td width="60%">
There is currently insufficient data about networking conditions to answer the query.  This is typically a transient state where qWAVE has erred on the side of caution as it awaits more data before ascertaining the state of the network.

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
</table>
 




## -remarks



If <a href="https://msdn.microsoft.com/36e4a71f-fb6b-42b6-a770-8cbcf98e7eb3">QOSStartTrackingClient</a> has not already been called, calling <b>QOSSetFlow</b> will cause the QOS subsystem to perform the following.<ul>
<li>Discover whether the end-to-end network path supports prioritization.</li>
<li>Track end-to-end network characteristics by way of network experiments.  These experiments do not place any noteworthy stress on the network.</li>
</ul>


If <b>QOSSetFlow</b> returns <b>ERROR_NETWORK_BUSY</b> there is insufficient bandwidth for the specified flow rate and network priority cannot be granted.  The application can still transmit a data stream but the flow will not receive priority marking.  Ideally an application would not attempt to stream at the requested rate if there is insufficient bandwidth. If <b>ERROR_NETWORK_BUSY</b> is returned the following safe strategy is available:<ol>
<li>Query the QoS subsystem with <a href="https://msdn.microsoft.com/e6d541fe-2aeb-4969-b138-869754dbdaa3">QOSNotifyFlow</a> in order to determine the current available bandwidth and begin to stream at the received lower rate with priority if the network supports it.</li>
<li>Request notification with <a href="https://msdn.microsoft.com/e6d541fe-2aeb-4969-b138-869754dbdaa3">QOSNotifyFlow</a> for when the originally desired amount of bandwidth is available.  When notification is received call  <b>QOSSetFlow</b> with the new bandwidth request and send at the new rate again with prioritization if supported.</li>
</ol>


This function may optionally be called asynchronously.


#### Examples

The following code snippet demonstrates the use of QOSSetFlow in an application. Input parameters <i>QOSHandle</i>, <i>FlowId</i>, <i>FlowId</i>, <i>QOSSetOutgoingRate</i>, and <b>sizeof</b>(<i>QoSOutgoingFlowrate</i>) must be  previously initialized by other QoS functions and calculations within the application.

Other QoS function examples that show initialization of parameters include <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>, <a href="https://msdn.microsoft.com/44136284-b553-446e-a95f-1eac476a7143">QOSAddSocketToFlow</a>, and <a href="https://msdn.microsoft.com/8cae3ba2-beca-45e2-9526-2d917abc2606">QOSQueryFlow</a>.

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>if( QOSSetFlow( QOSHandle,
        FlowId,
        QOSSetOutgoingRate,           // Operation 
        sizeof(QoSOutgoingFlowrate),  // Size
        &amp;QoSOutgoingFlowrate,         // Buffer
        0,                            // Flags (Must be set to 0 with QoS Version 1.0)
        NULL)                         // Overlapped
        == 0 )
{
    if( ERROR_INVALID_PARAMETER == GetLastError())
    {
        std::cerr &lt;&lt; __FILE__ &lt;&lt;" Line: " &lt;&lt; __LINE__ ;
        std::cerr &lt;&lt; " - QOSSetFlow failed. Exception code: "; 
        std::cerr &lt;&lt; GetLastError() &lt;&lt; " - Invalid parameter"; 
        std::cerr &lt;&lt; std::endl;
    }
    else
    {
        std::cerr &lt;&lt; __FILE__ &lt;&lt;" Line: " &lt;&lt; __LINE__ ;
        std::cerr &lt;&lt; " - QOSSetFlow failed. Exception code: "; 
        std::cerr &lt;&lt; GetLastError() &lt;&lt; std::endl;
    }
    
}
else
{
    std::cout &lt;&lt; "QOSSetFlow set outgoing flowrate bandwidth to "; 
    std::cout &lt;&lt; QoSOutgoingFlowrate.Bandwidth;
    std::cerr &lt;&lt; std::endl;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

