---
UID: NN:tapi3cc.ITAgentSession
title: ITAgentSession (tapi3cc.h)
author: windows-sdk-content
description: An agent session represents an association between an agent, group, and address.
old-location: tapi3\itagentsession.htm
tech.root: Tapi
ms.assetid: b0db0834-7b9b-4a72-9cc6-6cba31ed1275
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAgentSession, ITAgentSession interface [TAPI 2.2], ITAgentSession interface [TAPI 2.2],described, _tapi3_itagentsession, tapi3.itagentsession, tapi3cc/ITAgentSession
ms.topic: interface
f1_keywords: 
 - "tapi3cc/ITAgentSession"
req.header: tapi3cc.h
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
 - ITAgentSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentSession interface


## -description


An agent session represents an association between an agent, group, and address. The methods of 
<b>ITAgentSession</b> allow an application to retrieve a variety of statistics. The following methods create the 
<b>ITAgentSession</b> interface:


<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagentsession-next">IEnumAgentSession::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-get_agentsessions">ITAgent::get_AgentSessions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>


See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.

Note to TAPI 2.1 programmers: Many of the methods in this interface are COM wrappers for 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-linegetagentsessioninfo">lineGetAgentSessionInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentSession</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgentSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_acdcallrate">get_ACDCallRate</a>
</td>
<td align="left" width="63%">
Gets the ACD call rate per agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_acdgroup">get_ACDGroup</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itacdgroup">ITACDGroup</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_address">get_Address</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_agent">get_Agent</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_averagecalltime">get_AverageCallTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent per ACD call by this agent during this session, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_averagetalktime">get_AverageTalkTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent talking per ACD call by this agent during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_averagetimetoanswer">get_AverageTimeToAnswer</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) a call was waiting to be answered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_averagewrapuptime">get_AverageWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent on ACD call wrap-up during this agent session by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_longesttimetoanswer">get_LongestTimeToAnswer</a>
</td>
<td align="left" width="63%">
Gets the longest time (in seconds) a call was waiting to be answered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_numberofcalls">get_NumberOfCalls</a>
</td>
<td align="left" width="63%">
Gets the number of ACD calls handled by this agent during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_sessionduration">get_SessionDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the Agent session in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_sessionstarttime">get_SessionStartTime</a>
</td>
<td align="left" width="63%">
Gets the time that a session was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_state">get_State</a>
</td>
<td align="left" width="63%">
Gets the current 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a> of session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_totalcalltime">get_TotalCallTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD calls during this agent session by this agent, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_totaltalktime">get_TotalTalkTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent by this agent talking in ACD calls during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_totalwrapuptime">get_TotalWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD call wrap-up during this agent session by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-put_state">put_State</a>
</td>
<td align="left" width="63%">
Sets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a> of the session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

