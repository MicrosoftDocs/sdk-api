---
UID: NN:tapi3cc.ITTAPICallCenter
title: ITTAPICallCenter (tapi3cc.h)
description: The ITTAPICallCenter interface provides an entry point into call center controls.
old-location: tapi3\ittapicallcenter.htm
tech.root: Tapi
ms.assetid: 871cb217-a44f-421e-9cb4-7d8771335d08
ms.date: 12/05/2018
ms.keywords: ITTAPICallCenter, ITTAPICallCenter interface [TAPI 2.2], ITTAPICallCenter interface [TAPI 2.2],described, _tapi3_ittapicallcenter, tapi3.ittapicallcenter, tapi3cc/ITTAPICallCenter
f1_keywords:
- tapi3cc/ITTAPICallCenter
dev_langs:
- c++
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
- ITTAPICallCenter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPICallCenter interface


## -description


The 
<b>ITTAPICallCenter</b> interface provides an entry point into call center controls. It exposes methods that allow an application to discover available agent handlers. The agent handler interface can then be used to access the other elements of a call center, such as ACD groups, agents, and queues.

The 
<b>ITTAPICallCenter</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>.

Please see 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPICallCenter</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPICallCenter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPICallCenter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-enumerateagenthandlers">EnumerateAgentHandlers</a>
</td>
<td align="left" width="63%">
Enumerates 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interfaces currently associated with the call center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-get_agenthandlers">get_AgentHandlers</a>
</td>
<td align="left" width="63%">
Creates a collection of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interfaces currently associated with the call center. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-center-controls-interfaces">Call Center Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI Object</a>
 

 

