---
UID: NF:lpmapi.LPM_AdmitRsvpMsg
title: LPM_AdmitRsvpMsg function (lpmapi.h)
description: The LPM_AdmitRsvpMsg function is called by the PCM to pass RSVP messages to the LPM for policy-based admission control decisions.
helpviewer_keywords: ["ErrorSpec","FlowDescList","FlowDescListCount","LPM_AdmitRsvpMsg","LPM_AdmitRsvpMsg callback","LPM_AdmitRsvpMsg callback function [QOS]","LpmPriorityValue","PolicyDataCount","PolicyDataObjects","PolicyErrorCode","PolicyErrorValue","RsvpFromHop","RsvpMsgType","RsvpScope","RsvpSession","RsvpStyle","_gqos_lpm_admitrsvpmsg","lpmapi/LPM_AdmitRsvpMsg","qos.lpm_admitrsvpmsg"]
old-location: qos\lpm_admitrsvpmsg.htm
tech.root: QOS
ms.assetid: 0bf84c25-312c-4b4a-8bb1-e8f00711dbe3
ms.date: 12/05/2018
ms.keywords: ErrorSpec, FlowDescList, FlowDescListCount, LPM_AdmitRsvpMsg, LPM_AdmitRsvpMsg callback, LPM_AdmitRsvpMsg callback function [QOS], LpmPriorityValue, PolicyDataCount, PolicyDataObjects, PolicyErrorCode, PolicyErrorValue, RsvpFromHop, RsvpMsgType, RsvpScope, RsvpSession, RsvpStyle, _gqos_lpm_admitrsvpmsg, lpmapi/LPM_AdmitRsvpMsg, qos.lpm_admitrsvpmsg
req.header: lpmapi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPM_AdmitRsvpMsg
 - lpmapi/LPM_AdmitRsvpMsg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_AdmitRsvpMsg
---

# LPM_AdmitRsvpMsg function


## -description

The 
<i>LPM_AdmitRsvpMsg</i> function is called by the PCM to pass RSVP messages to the LPM for policy based–admission control decisions. Results from calling 
<i>LPM_AdmitRsvpMsg</i> can be passed back to the PCM either synchronously or asynchronously by setting the return value appropriately. Asynchronous results should be returned by calling the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbadmitresult">cbAdmitResult</a> function.

## -parameters

### -param PcmReqHandle [in]

Unique handle that identifies this request from all other requests. LPMs must pass this handle to the PCM when returning results asynchronously for an individual request by calling 
<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbadmitresult">cbAdmitResult</a>. The <i>PcmReqHandle</i> parameter becomes invalid once results are returned, requiring each request to get its own unique <i>PcmReqHandle</i> from the PCM.

### -param pRecvdIntf [in]

Pointer to the interface on which the message was received. The received interface IP address is supplied as the RSVP HOP object, and the Logical Interface Handle is set to the SNMP Index. Note that interface index numbers can change with the addition and deletion of interfaces, due to the Plug and Play features of Windows 2000.

### -param pRsvpMsgObjs [in]

Objects received from RSVP. The SBM unpacks received RSVP messages into individual objects and converts the contents of such RSVP objects into host order, and supplies them in the <b>RSVP_MSG_OBJS</b> structure, which is defined in Lpmapi.h. The following objects are supplied.

### -param RcvdRsvpMsgLength [in]

Length of the received RSVP message, in bytes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RsvpMsgType"></a><a id="rsvpmsgtype"></a><a id="RSVPMSGTYPE"></a><dl>
<dt><b>RsvpMsgType</b></dt>
</dl>
</td>
<td width="60%">
RSVP message type, as defined by the RSVP protocol.

</td>
</tr>
<tr>
<td width="40%"><a id="RsvpSession"></a><a id="rsvpsession"></a><a id="RSVPSESSION"></a><dl>
<dt><b>RsvpSession</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the RSVP session, as defined by the RSVP protocol. Note that contents are in host order.

</td>
</tr>
<tr>
<td width="40%"><a id="RsvpFromHop"></a><a id="rsvpfromhop"></a><a id="RSVPFROMHOP"></a><dl>
<dt><b>RsvpFromHop</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the hop from which the RSVP message was received. Note that contents are in host order.

</td>
</tr>
<tr>
<td width="40%"><a id="RsvpScope"></a><a id="rsvpscope"></a><a id="RSVPSCOPE"></a><dl>
<dt><b>RsvpScope</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the RSVP scope object.

</td>
</tr>
<tr>
<td width="40%"><a id="RsvpStyle"></a><a id="rsvpstyle"></a><a id="RSVPSTYLE"></a><dl>
<dt><b>RsvpStyle</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the RSVP reservation style, as defined by the RSVP protocol. Note that contents are in host order.

</td>
</tr>
<tr>
<td width="40%"><a id="FlowDescListCount"></a><a id="flowdesclistcount"></a><a id="FLOWDESCLISTCOUNT"></a><dl>
<dt><b>FlowDescListCount</b></dt>
</dl>
</td>
<td width="60%">
Number of flow descriptors.

</td>
</tr>
<tr>
<td width="40%"><a id="FlowDescList"></a><a id="flowdesclist"></a><a id="FLOWDESCLIST"></a><dl>
<dt><b>FlowDescList</b></dt>
</dl>
</td>
<td width="60%">
Array of flow descriptor pointers.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyDataCount"></a><a id="policydatacount"></a><a id="POLICYDATACOUNT"></a><dl>
<dt><b>PolicyDataCount</b></dt>
</dl>
</td>
<td width="60%">
Number of policy data objects.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyDataObjects"></a><a id="policydataobjects"></a><a id="POLICYDATAOBJECTS"></a><dl>
<dt><b>PolicyDataObjects</b></dt>
</dl>
</td>
<td width="60%">
Array of policy data object pointers. Note that only the RSVP object header and the policy options are converted to host order, but policy element headers as well as contents are left in network order; the PCM cannot convert the latter to host order, because the PCM cannot parse policy elements. Note that the Microsoft-provided LPM, Msidlpm.dll, does reorder policy element content into host order.

</td>
</tr>
<tr>
<td width="40%"><a id="ErrorSpec"></a><a id="errorspec"></a><a id="ERRORSPEC"></a><dl>
<dt><b>ErrorSpec</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the received RSVP ERROR_SPEC object.

</td>
</tr>
</table>

### -param RcvdRsvpMsg [in]

RSVP message, in network order.

### -param pulPcmActionFlags [out]

Flags used to specify an action requested of the PCM. The LPM can currently set this parameter to FORCE_IMMEDIATE_REFRESH to request an immediate refresh of the message being admitted. An LPM can set this flag if a change in policy data is detected that it wants to forward immediately. Before sending, the SBM asks the LPM to supply policy information for the outgoing refresh message.


Note that LPMs do not need to set this flag when a new PATH message is being accepted; SBMs automatically send the new PATH message toward receivers.

### -param pPolicyDecisions [out]

Pointer to policy decisions. An LPM must allocate this buffer using the memory allocator supplied in the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> function call; the SBM frees the buffer after acting on <i>pPolicyDecisions</i>. The PCM looks at <i>pPolicyDecisions</i> only when the function returns LPM_RESULT_READY. Synchronous policy decisions must be returned for each flow in <i>FlowDescList</i>, and the number of entries in the <i>pPolicyDecisions</i> array must be equal to <i>FlowDescListCount</i>. Each policy decision consists of the values shown in the following table. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LpmPriorityValue"></a><a id="lpmpriorityvalue"></a><a id="LPMPRIORITYVALUE"></a><dl>
<dt><b>LpmPriorityValue</b></dt>
</dl>
</td>
<td width="60%">
Pointer to a buffer to receive the LPM Priority Value from the LPM. Note that the PCM will only look at this parameter if the return value of 
<i>LPM_AdmitRsvpMsg</i> is set to LPM_RESULT_READY. If the LPM is returning results synchronously, this parameter must be set to a valid priority value. See 
<a href="/previous-versions/windows/desktop/qos/local-policy-module">Local Policy Module</a> for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyErrorCode"></a><a id="policyerrorcode"></a><a id="POLICYERRORCODE"></a><dl>
<dt><b>PolicyErrorCode</b></dt>
</dl>
</td>
<td width="60%">
Pointer to a policy error code. If the request is being rejected synchronously, LPMs must provide a nonzero value for this parameter; the SBM will copy this value, in combination with <i>PolicyErrorValue</i>, into the RSVP error object when sending PATHERR or RESVERR messages (as the result of policy based–admission control failure, to provide a reason for rejecting the request).

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyErrorValue"></a><a id="policyerrorvalue"></a><a id="POLICYERRORVALUE"></a><dl>
<dt><b>PolicyErrorValue</b></dt>
</dl>
</td>
<td width="60%">
Pointer to a policy error value. If the request is being rejected synchronously, LPMs must provide a nonzero value for this parameter; the SBM will copy this value, in combination with <i>PolicyErrorCode</i>, into the RSVP error object when sending PATHERR or RESVERR messages (as the result of policy based–admission control failure, to provide a reason for rejecting the request).

</td>
</tr>
</table>
 

Since an LPM's return POLICY_DECISION is an array, an LPM can accept a subset of flows in <i>FlowDescList</i> and reject the rest of them, if appropriate. For example, since FF style RESV messages can contain multiple flows, when an LPM rejects some flows and accepts others, the SBM generates a separate RESVERR message for each rejected flow; before sending the RESVERR message, PCM calls each LPM to supply policy data objects for each outgoing RESVERR message.

### -param Reserved [out]

Reserved for future use.

## -returns

This function returns ULONG.

## -remarks

The Subnet Bandwidth Manager (SBM) forwards RSVP PATH, RESV, PATHERR, RESVERR, PATH_TEAR, and RESV_TEAR messages to the PCM. If a request passes LPM policy–based admission (in which case the success status is passed up through the PCM to the SBM), the SBM performs resource based–admission control as part of its RSVP processing; if resource based–admission control fails, the SBM will instruct the PCM to instruct each LPM to delete its state through the 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_commitresv">LPM_CommitResv</a> function. In such circumstances, the SBM (and not the LPMs) will create the requisite RSVP error message.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbadmitresult">cbAdmitResult</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-cbgetrsvpobjects">cbGetRsvpObjects</a>
