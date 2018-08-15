---
UID: NN:tapi3cc.ITAgent
title: ITAgent
author: windows-sdk-content
description: Agents are the heart of a call center.
old-location: tapi3\itagent.htm
old-project: tapi
ms.assetid: 6c1409c9-da73-4d21-bf56-07e9ab7b33a0
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgent, ITAgent interface [TAPI 2.2], ITAgent interface [TAPI 2.2],described, _tapi3_itagent, tapi3.itagent, tapi3cc/ITAgent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3cc.h
req.include-header: Tapi3.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent interface


## -description


Agents are the heart of a call center. They are responsible for receiving and processing incoming calls and, at times, making outgoing calls to customers or prospects. The following methods create the 
<b>ITAgent</b> interface:


<a href="https://msdn.microsoft.com/68a7842c-557a-4da4-aa2b-e7c15a6d4f4a">IEnumAgent::Next</a>



<a href="https://msdn.microsoft.com/90a1684d-5cb0-4d1b-ac38-b03f9f1ff838">ITAgentEvent::get_Agent</a>



<a href="https://msdn.microsoft.com/f3242013-59a6-40f9-9bb1-0bc30f27311c">ITAgentHandler::CreateAgent</a>


See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAgent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68cc2ffe-3c63-4723-8652-0e28da2b17b6">CreateSession</a>
</td>
<td align="left" width="63%">
Creates a new agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d901ad31-8ccc-4bca-9413-dff838a33088">CreateSessionWithPIN</a>
</td>
<td align="left" width="63%">
Creates a new agent session, with Personal Identification Number (PIN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b639a41-c866-49ad-bc33-1215da7c8a19">EnumerateAgentSessions</a>
</td>
<td align="left" width="63%">
Enumerates the current agent sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25503eae-ebee-4b57-ab5c-b3f152de9a96">get_AgentSessions</a>
</td>
<td align="left" width="63%">
Creates a collection of current agent sessions. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5045dd7-5a12-415e-b68a-f483f77f4887">get_ID</a>
</td>
<td align="left" width="63%">
Gets an agent's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccc91dfb-83e5-496a-921d-784fcaea5af5">get_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Gets the period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bef36468-8ee9-4ce2-bf8d-e2bd8c986ae3">get_NumberOfACDCalls</a>
</td>
<td align="left" width="63%">
Gets the number of ACD calls handled by this agent across all sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d70073e9-a181-4f8d-b34f-95c8a24fe8d6">get_NumberOfIncomingCalls</a>
</td>
<td align="left" width="63%">
Gets the number of incoming non-ACD calls handled by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb2af58c-0b9e-4b00-8d8c-2fbfb2e0fc95">get_NumberOfOutgoingCalls</a>
</td>
<td align="left" width="63%">
Gets the number of outgoing non-ACD calls handled by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea85f3a7-0081-4ce2-bf2e-c47e6e7c4cbb">get_OverallCallRate</a>
</td>
<td align="left" width="63%">
Gets the agent call rate across all sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6690a62b-65a1-4892-aeee-4a6652939d5f">get_State</a>
</td>
<td align="left" width="63%">
Gets the state of an agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/432e22b7-16c3-447d-bbec-59ab7713039c">get_TotalACDCallTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD calls by this agent, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a622a812-c929-413a-a3bc-4e870158cf16">get_TotalACDTalkTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent talking in ACD calls by this agent (across all sessions).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23fb0c9b-b3c7-4a1d-91fc-9ecfb6a2d8bf">get_TotalWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD wrap-up work by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6949fdb0-5841-4473-bb50-2ea598a71576">get_User</a>
</td>
<td align="left" width="63%">
Gets the agent user name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c5d6e8e-8ddf-4eef-be79-fed56daecb1b">put_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Sets the period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f75146c-d8ce-4e9d-91bf-15dbb31b5c88">put_State</a>
</td>
<td align="left" width="63%">
Sets the state of an agent session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

