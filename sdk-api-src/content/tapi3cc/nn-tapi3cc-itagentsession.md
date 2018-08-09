---
UID: NN:tapi3cc.ITAgentSession
title: ITAgentSession
author: windows-sdk-content
description: An agent session represents an association between an agent, group, and address.
old-location: tapi3\itagentsession.htm
old-project: tapi
ms.assetid: b0db0834-7b9b-4a72-9cc6-6cba31ed1275
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgentSession, ITAgentSession interface [TAPI 2.2], ITAgentSession interface [TAPI 2.2],described, _tapi3_itagentsession, tapi3.itagentsession, tapi3cc/ITAgentSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITAgentSession
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSession interface


## -description


An agent session represents an association between an agent, group, and address. The methods of 
<b>ITAgentSession</b> allow an application to retrieve a variety of statistics. The following methods create the 
<b>ITAgentSession</b> interface:


<a href="https://msdn.microsoft.com/5ac647a0-7f1a-4f6a-ad01-dba019f9bf56">IEnumAgentSession::Next</a>



<a href="https://msdn.microsoft.com/25503eae-ebee-4b57-ab5c-b3f152de9a96">ITAgent::get_AgentSessions</a>



<a href="https://msdn.microsoft.com/68cc2ffe-3c63-4723-8652-0e28da2b17b6">ITAgent::CreateSession</a>


See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.

Note to TAPI 2.1 programmers: Many of the methods in this interface are COM wrappers for 
<a href="https://msdn.microsoft.com/06a5ea23-4205-46fd-abe7-ee4575be81c8">lineGetAgentSessionInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentSession</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAgentSession</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/49737945-7e27-4c88-94c5-29db7dccfc97">get_ACDCallRate</a>
</td>
<td align="left" width="63%">
Gets the ACD call rate per agent session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec80092d-ceff-432c-ba0a-695718b890af">get_ACDGroup</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/addd088d-5bca-4865-8cae-3c013554dafd">get_Address</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1378f7f1-020e-492c-8f1a-f4e8a9c7c3e2">get_Agent</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a> associated with this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05029076-cb76-4771-b0a8-0c09e184e6ee">get_AverageCallTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent per ACD call by this agent during this session, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6025053-b21f-478e-86d7-a8572ed2b205">get_AverageTalkTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent talking per ACD call by this agent during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24d2b9ee-4fd0-41d3-add1-5c136944a250">get_AverageTimeToAnswer</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) a call was waiting to be answered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/365d98ab-9127-45bb-8232-3e3903bd9ab3">get_AverageWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the average time (in seconds) spent on ACD call wrap-up during this agent session by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aca11b6d-7656-4162-9bf7-1b8ffaa487de">get_LongestTimeToAnswer</a>
</td>
<td align="left" width="63%">
Gets the longest time (in seconds) a call was waiting to be answered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a3f00fc-9da2-4dc9-ab9a-ebc92664e907">get_NumberOfCalls</a>
</td>
<td align="left" width="63%">
Gets the number of ACD calls handled by this agent during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5cb6bd2-3b3e-442a-b766-bdd9254475dc">get_SessionDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the Agent session in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84c73a96-9748-430f-8653-55656eadc617">get_SessionStartTime</a>
</td>
<td align="left" width="63%">
Gets the time that a session was created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85a389ee-2d6c-4607-873a-8ca0c16a0fac">get_State</a>
</td>
<td align="left" width="63%">
Gets the current 
<a href="https://msdn.microsoft.com/0c902924-e142-4ab9-9b20-661d7c2e3629">AGENT_SESSION_STATE</a> of session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d6aee4-0d50-42da-8e2e-db9d3731cb3c">get_TotalCallTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD calls during this agent session by this agent, including wrap-up time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57871df2-cd9b-440b-ab33-51a8eb7398c1">get_TotalTalkTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent by this agent talking in ACD calls during this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b1cda40-36bd-481a-bc59-81b810ebed09">get_TotalWrapUpTime</a>
</td>
<td align="left" width="63%">
Gets the number of seconds spent on ACD call wrap-up during this agent session by this agent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d35bacd-c4e4-4c31-b946-ad76ffb250ed">put_State</a>
</td>
<td align="left" width="63%">
Sets the 
<a href="https://msdn.microsoft.com/0c902924-e142-4ab9-9b20-661d7c2e3629">AGENT_SESSION_STATE</a> of the session.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

