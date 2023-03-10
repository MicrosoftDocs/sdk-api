---
UID: NS:qos._flowspec
title: FLOWSPEC (qos.h)
description: The FLOWSPEC structure provides quality of service parameters to the RSVP SP.
helpviewer_keywords: ["*LPFLOWSPEC","*PFLOWSPEC","FLOWSPEC","FLOWSPEC structure [QOS]","LPFLOWSPEC","LPFLOWSPEC structure pointer [QOS]","PFLOWSPEC","PFLOWSPEC structure pointer [QOS]","SERVICETYPE_BESTEFFORT","SERVICETYPE_CONTROLLEDLOAD","SERVICETYPE_GENERAL_INFORMATION","SERVICETYPE_GUARANTEED","SERVICETYPE_NETWORK_CONTROL","SERVICETYPE_NETWORK_UNAVAILBLE","SERVICETYPE_NOCHANGE","SERVICETYPE_NONCONFORMING","SERVICETYPE_NOTRAFFIC","SERVICETYPE_QUALITATIVE","SERVICE_NO_QOS_SIGNALING","SERVICE_NO_TRAFFIC_CONTROL","_gqos_flowspec","qos.flowspec","qos/FLOWSPEC","qos/LPFLOWSPEC","qos/PFLOWSPEC"]
old-location: qos\flowspec.htm
tech.root: QOS
ms.assetid: 268e0d3a-2b04-40fd-91eb-f1780236b3e4
ms.date: 12/05/2018
ms.keywords: '*LPFLOWSPEC, *PFLOWSPEC, FLOWSPEC, FLOWSPEC structure [QOS], LPFLOWSPEC, LPFLOWSPEC structure pointer [QOS], PFLOWSPEC, PFLOWSPEC structure pointer [QOS], SERVICETYPE_BESTEFFORT, SERVICETYPE_CONTROLLEDLOAD, SERVICETYPE_GENERAL_INFORMATION, SERVICETYPE_GUARANTEED, SERVICETYPE_NETWORK_CONTROL, SERVICETYPE_NETWORK_UNAVAILBLE, SERVICETYPE_NOCHANGE, SERVICETYPE_NONCONFORMING, SERVICETYPE_NOTRAFFIC, SERVICETYPE_QUALITATIVE, SERVICE_NO_QOS_SIGNALING, SERVICE_NO_TRAFFIC_CONTROL, _gqos_flowspec, qos.flowspec, qos/FLOWSPEC, qos/LPFLOWSPEC, qos/PFLOWSPEC'
req.header: qos.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FLOWSPEC, *PFLOWSPEC, *LPFLOWSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _flowspec
 - qos/_flowspec
 - PFLOWSPEC
 - qos/PFLOWSPEC
 - FLOWSPEC
 - qos/FLOWSPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos.h
api_name:
 - FLOWSPEC
---

# FLOWSPEC structure


## -description

The 
<b>FLOWSPEC</b> structure provides quality of service parameters to the 
<a href="/previous-versions/windows/desktop/qos/rsvp-service-provider">RSVP SP</a>. This allows QOS-aware applications to invoke, modify, or remove QOS settings for a given flow. Some members of 
<b>FLOWSPEC</b> can be set to default values. See Remarks for more information.

## -struct-fields

### -field TokenRate

Specifies the permitted rate at which data can be transmitted over the life of the flow. The <b>TokenRate</b> member is similar to other token bucket models seen in such WAN technologies as Frame Relay, in which the token is analogous to a credit. If such tokens are not used immediately, they accrue to allow data transmission up to a certain periodic limit (<b>PeakBandwidth</b>, in the case of Windows 2000 quality of service). Accrual of credits is limited, however, to a specified amount (<b>TokenBucketSize</b>). Limiting total credits (tokens) avoids situations where, for example, flows that are inactive for some time flood the available bandwidth with their large amount of accrued tokens. Because flows may accrue transmission credits over time (at their <b>TokenRate</b> value) only up to the maximum of their <b>TokenBucketSize</b>, and because they are limited in burst transmissions to their <b>PeakBandwidth</b>, traffic control and network-device resource integrity are maintained. 
<a href="/previous-versions/windows/desktop/qos/understanding-traffic-control">Traffic control</a> is maintained because flows cannot send too much data at once, and network-device resource integrity is maintained because such devices are spared high traffic bursts. 




With this model, applications can transmit data only when sufficient credits are available. If sufficient credits are not available, the application must either wait or discard the traffic (based on the value of 
<a href="/windows/desktop/api/qos/ns-qos-qos_sd_mode">QOS_SD_MODE</a>). Therefore, it is important that applications base their <b>TokenRate</b> requests on reasonable expectations for transmission requirements. For example, in video applications, <b>TokenRate</b> is typically set to the average bit rate from peak to peak.

If <b>TokenRate</b> is set to QOS_NOT_SPECIFIED on the receiver only, the maximum transmission unit (MTU) is used for <b>TokenRate</b>, and limits on the transmission rate (the token bucket model) will not be put into effect. Thus, <b>TokenRate</b> is expressed in bytes per second.

The <b>TokenRate</b> member cannot be set to zero. Nor can it be set as a default (that is, set to QOS_NOT_SPECIFIED) in a sending 
<b>FLOWSPEC</b>.

### -field TokenBucketSize

The maximum amount of credits a given direction of a flow can accrue, regardless of time, in bytes. In video applications, <b>TokenBucketSize</b> will likely be the largest average frame size. In constant rate applications, <b>TokenBucketSize</b> should be set to allow for small variations.

### -field PeakBandwidth

The upper limit on time-based transmission permission for a given flow, in bytes per second. The <b>PeakBandwidth</b> member restricts flows that may have accrued a significant amount of transmission credits, or tokens from overburdening network resources with one-time or cyclical data bursts, by enforcing a per-second data transmission ceiling. Some intermediate systems can take advantage of this information, resulting in more efficient resource allocation.

### -field Latency

Maximum acceptable delay between transmission of a bit by the sender and its receipt by one or more intended receivers, in microseconds. The precise interpretation of this number depends on the level of guarantee specified in the QOS request.

### -field DelayVariation

Difference between the maximum and minimum possible delay a packet will experience, in microseconds. Applications use <b>DelayVariation</b> to determine the amount of buffer space needed at the receiving end of the flow. This buffer space information can be used to restore the original data transmission pattern.

### -field ServiceType

Specifies the level of service to negotiate for the flow. The <b>ServiceType</b> member can be one of the following defined service types. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOTRAFFIC"></a><a id="servicetype_notraffic"></a><dl>
<dt><b>SERVICETYPE_NOTRAFFIC</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no traffic will be transmitted in the specified direction. On duplex-capable media, this value signals underlying software to set up unidirectional connections only. This service type is not valid for the TC API.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_BESTEFFORT"></a><a id="servicetype_besteffort"></a><dl>
<dt><b>SERVICETYPE_BESTEFFORT</b></dt>
</dl>
</td>
<td width="60%">
Results in no action taken by the RSVP SP. Traffic control does create a BESTEFFORT flow, however, and traffic on the flow will be handled by traffic control similarly to other BESTEFFORT traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_CONTROLLEDLOAD"></a><a id="servicetype_controlledload"></a><dl>
<dt><b>SERVICETYPE_CONTROLLEDLOAD</b></dt>
</dl>
</td>
<td width="60%">
Provides an end-to-end QOS that closely approximates transmission quality provided by best-effort service, as expected under unloaded conditions from the associated network components along the data path. 




Applications that use SERVICETYPE_CONTROLLEDLOAD may therefore assume the following:

<ul>
<li>The network will deliver a very high percentage of transmitted packets to its intended receivers. In other words, packet loss will closely approximate the basic packet error rate of the transmission medium.</li>
<li>Transmission delay for a very high percentage of the delivered packets will not greatly exceed the minimum transit delay experienced by any successfully delivered packet.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GUARANTEED"></a><a id="servicetype_guaranteed"></a><dl>
<dt><b>SERVICETYPE_GUARANTEED</b></dt>
</dl>
</td>
<td width="60%">
Guarantees that datagrams will arrive within the guaranteed delivery time and will not be discarded due to queue overflows, provided the flow's traffic stays within its specified traffic parameters. This service is intended for applications that need a firm guarantee that a datagram will arrive no later than a certain time after it was transmitted by its source.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_QUALITATIVE"></a><a id="servicetype_qualitative"></a><dl>
<dt><b>SERVICETYPE_QUALITATIVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the application requires better than BESTEFFORT transmission, but cannot quantify its transmission requirements. Applications that use SERVICETYPE_QUALITATIVE can supply an application identifier policy object. The application identification policy object enables policy servers on the network to identify the application, and accordingly, assign an appropriate quality of service to the request. For more information on application identification, consult the IETF Internet Draft draft-ietf-rap-rsvp-appid-00.txt, or the Microsoft white paper on Application Identification. Traffic control treats flows of this type with the same priority as BESTEFFORT traffic on the local computer. However, application programmers can get boosted priority for such flows by modifying the Layer 2 settings on the associated flow using the 
<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_traffic_class">QOS_TRAFFIC_CLASS</a> QOS object.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_UNAVAILBLE"></a><a id="servicetype_network_unavailble"></a><dl>
<dt><b>SERVICETYPE_NETWORK_UNAVAILBLE</b></dt>
</dl>
</td>
<td width="60%">
Used to notify network changes.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_CONTROL"></a><a id="servicetype_network_control"></a><dl>
<dt><b>SERVICETYPE_NETWORK_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
Used only for transmission of control packets (such as RSVP signaling messages). This <b>ServiceType</b> has the highest priority.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GENERAL_INFORMATION"></a><a id="servicetype_general_information"></a><dl>
<dt><b>SERVICETYPE_GENERAL_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
Specifies that all service types are supported for a flow. Can be used on sender side only.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOCHANGE"></a><a id="servicetype_nochange"></a><dl>
<dt><b>SERVICETYPE_NOCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the quality of service in the transmission using this <b>ServiceType</b> value is not changed. SERVICETYPE_NOCHANGE can be used when requesting a change in the quality of service for one direction only, or when requesting a change only within the ProviderSpecific parameters of a QOS specification, and not in the <b>SendingFlowspec</b> or <b>ReceivingFlowspec</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NONCONFORMING"></a><a id="servicetype_nonconforming"></a><dl>
<dt><b>SERVICETYPE_NONCONFORMING</b></dt>
</dl>
</td>
<td width="60%">
Used to indicate nonconforming traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NO_TRAFFIC_CONTROL"></a><a id="service_no_traffic_control"></a><dl>
<dt><b>SERVICE_NO_TRAFFIC_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that traffic control should not be invoked in the specified direction.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_NO_QOS_SIGNALING"></a><a id="service_no_qos_signaling"></a><dl>
<dt><b>SERVICE_NO_QOS_SIGNALING</b></dt>
</dl>
</td>
<td width="60%">
Suppresses RSVP signaling in the specified direction.

</td>
</tr>
</table>
 

The following list identifies the relative priority of <b>ServiceType</b> settings:

SERVICETYPE_NETWORK_CONTROL

SERVICETYPE_GUARANTEED

SERVICETYPE_CONTROLLED_LOAD

SERVICETYPE_BESTEFFORT

SERVICETYPE_QUALITATIVE

Non-conforming traffic
						

For a simple example, if a given network device were resource-bounded and had to choose among transmitting a packet from one of the above <b>ServiceType</b> settings, it would first send a packet of SERVICETYPE_NETWORKCONTROL, and if there were no packets of that <b>ServiceType</b> requiring transmission it would send a packet of <b>ServiceType</b> SERVICETYPE_GUARANTEED, and so on.

### -field MaxSduSize

Specifies the maximum packet size permitted or used in the traffic flow, in bytes.

### -field MinimumPolicedSize

Specifies the minimum packet size for which the requested quality of service will be provided, in bytes. Packets smaller than this size are treated by traffic control as <b>MinimumPolicedSize</b>. When using the <b>FLOWSPEC</b> structure in association with RSVP, the value of <b>MinimumPolicedSize</b> cannot be zero; however, if you are using the <b>FLOWSPEC</b> structure specifically with the TC API, you can set <b>MinimumPolicedSize</b> to zero.

## -remarks

Many members of the 
<b>FLOWSPEC</b> structure can be set to default values by setting the member to QOS_NOT_SPECIFIED. Note that the members that can be set to default values differ depending on whether the 
<b>FLOWSPEC</b> is a receiving 
<b>FLOWSPEC</b> or a sending 
<b>FLOWSPEC</b>.

There are a handful of considerations you should keep in mind when using 
<b>FLOWSPEC</b> with traffic control:

<ul>
<li><b>TokenRate</b> can be QOS_NOT_SPECIFIED for SERVICETYPE_NETWORKCONTROL, SERVICETYPE_QUALITATIVE, and SERVICETYPE_BESTEFFORT. <b>TokenRate</b> must be valid for all other <b>ServiceType</b> values.</li>
<li>If <b>PeakBandwidth</b> is specified, it must be greater than or equal to <b>TokenRate</b>.</li>
</ul>
Many settings can be defaulted in a receiving 
<b>FLOWSPEC</b> except <b>ServiceType</b>, with the following considerations:

<ul>
<li>For a Controlled Load Service receiver, the default values are derived from the sender <b>TSPEC</b>.</li>
<li>For a Guaranteed Service receiver, <b>ServiceType</b> and <b>TokenRate</b> must be specified.</li>
</ul>
The following list specifies the values that are applied when a receiving 
<b>FLOWSPEC</b> sets the corresponding values to default:



When the value of the <b>ServiceType</b> is set to SERVICETYPE_GUARANTEED, the following also applies:

<ul>
<li>The RATE value in <b>RSPEC</b> is set to the value of <i>TokenRate</i>.</li>
<li>The DELAYSLACKTERM value in <b>RSPEC</b> is set to <i>DelayVariation</i>, which is set to zero if <i>DelayVariation</i> is set to QOS_NOT_SPECIFIED.</li>
<li>For receivers requesting SERVICETYPE_GUARANTEED, the receiving <i>TokenRate</i> must be specified. This contrasts with a SERVICETYPE_CONTROLLEDLOAD receiver, for which <i>TokenRate</i> may be set to QOS_NOT_SPECIFIED.</li>
</ul>
In a sending 
<b>FLOWSPEC</b>, everything can be defaulted except <b>ServiceType</b> and <b>TokenRate</b>. The following list specifies the values that are applied when a sending 
<b>FLOWSPEC</b> sets the corresponding values to default:



<b>Traffic Control:  </b>The following <b>ServiceType</b>s are invalid when specifically working with Traffic Control. If you are unsure whether you are working directly with Traffic Control (and thereby need to be concerned about whether the following <b>ServiceType</b>s are applicable in your situation), you probably are not:<dl>
<dd>SERVICE_NO_TRAFFIC_CONTROL</dd>
<dd>SERVICE_NO_QOS_SIGNALING</dd>
<dd>SERVICETYPE_GENERAL_INFORMATION</dd>
<dd>SERVICETYPE_NETWORK_UNAVAILABLE</dd>
<dd>SERVICETYPE_NOCHANGE</dd>
<dd>SERVICETYPE_NOTRAFFIC</dd>
</dl>

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>