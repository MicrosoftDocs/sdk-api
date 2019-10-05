---
UID: NN:tapi3.ITAgent
title: ITAgent (tapi3.h)
author: windows-sdk-content
description: Agents are the heart of a call center.
old-location: tapi3\itagent.htm
tech.root: Tapi
ms.assetid: 6c1409c9-da73-4d21-bf56-07e9ab7b33a0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAgent, ITAgent interface [TAPI 2.2], ITAgent interface [TAPI 2.2],described, _tapi3_itagent, tapi3.itagent, tapi3cc/ITAgent
ms.topic: interface
f1_keywords: 
 - "tapi3/ITAgent"
dev_langs:
 - c++
req.header: tapi3.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgent interface


## -description


Agents are the heart of a call center. They are responsible for receiving and processing incoming calls and, at times, making outgoing calls to customers or prospects. The following methods create the 
<b>ITAgent</b> interface:


<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagent-next">IEnumAgent::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentevent-get_agent">ITAgentEvent::get_Agent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagent">ITAgentHandler::CreateAgent</a>


See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">CreateSession</a>
</td>
<td align="left" width="63%">
Creates a new agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-createsessionwithpin">CreateSessionWithPIN</a>
</td>
<td align="left" width="63%">
Creates a new agent session, with Personal Identification Number (PIN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-enumerateagentsessions">EnumerateAgentSessions</a>
</td>
<td align="left" width="63%">
Enumerates the current agent sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_agentsessions">get_AgentSessions</a>
</td>
<td align="left" width="63%">
Creates a collection of current agent sessions. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_id">get_ID</a>
</td>
<td align="left" width="63%">
Gets an agent's ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_measurementperiod">get_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Gets the period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_numberofacdcalls">get_NumberOfACDCalls</a>
</td>
<td align="left" width="63%">
Gets the number of ACD calls handled by this agent across all sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_numberofincomingcalls">get_NumberOfIncomingCalls</a>
</td>
<td align="left" width="63%">
Gets the number of incoming non-ACD calls handled by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_numberofoutgoingcalls">get_NumberOfOutgoingCalls</a>
</td>
<td align="left" width="63%">
Gets the number of outgoing non-ACD calls handled by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_overallcallrate">get_OverallCallRate</a>
</td>
<td align="left" width="63%">
Gets the agent call rate across all sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_state">get_State</a>
</td>
<td align="left" width="63%">
Gets the state of an agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_totalacdcalltime">get_TotalACDCallTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD calls by this agent, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_totalacdtalktime">get_TotalACDTalkTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent talking in ACD calls by this agent (across all sessions).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_totalwrapuptime">get_TotalWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD wrap-up work by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_user">get_User</a>
</td>
<td align="left" width="63%">
Gets the agent user name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-put_measurementperiod">put_MeasurementPeriod</a>
</td>
<td align="left" width="63%">
Sets the period (in seconds) for which the switch and/or implementation stores and calculates information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-put_state">put_State</a>
</td>
<td align="left" width="63%">
Sets the state of an agent session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

