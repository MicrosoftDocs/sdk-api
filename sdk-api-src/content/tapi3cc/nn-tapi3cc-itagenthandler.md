---
UID: NN:tapi3cc.ITAgentHandler
title: ITAgentHandler (tapi3cc.h)
description: The ITAgentHandler interface provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups. The IEnumAgentHandler::Next and ITTapiCallCenter::get_AgentHandlers methods create the ITAgentHandler interface.
old-location: tapi3\itagenthandler.htm
tech.root: Tapi
ms.assetid: 11861d77-39ad-4d85-bf68-ba0f4321ba7c
ms.date: 12/05/2018
ms.keywords: ITAgentHandler, ITAgentHandler interface [TAPI 2.2], ITAgentHandler interface [TAPI 2.2],described, _tapi3_itagenthandler, tapi3.itagenthandler, tapi3cc/ITAgentHandler
f1_keywords:
- tapi3cc/ITAgentHandler
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
- ITAgentHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentHandler interface


## -description


The 
<b>ITAgentHandler</b> interface provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-next">IEnumAgentHandler::Next</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-get_agenthandlers">ITTapiCallCenter::get_AgentHandlers</a> methods create the 
<b>ITAgentHandler</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentHandler</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgentHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagent">CreateAgent</a>
</td>
<td align="left" width="63%">
Creates an Agent object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagentwithid">CreateAgentWithID</a>
</td>
<td align="left" width="63%">
Creates an Agent object based on an agent identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateacdgroups">EnumerateACDGroups</a>
</td>
<td align="left" width="63%">
Enumerates ACD groups currently associated with the agent handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateusableaddresses">EnumerateUsableAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses available for receiving ACD calls on this agent handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_acdgroups">get_ACDGroups</a>
</td>
<td align="left" width="63%">
Creates a collection of ACD groups currently associated with the agent handler. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the agent handler name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_usableaddresses">get_UsableAddresses</a>
</td>
<td align="left" width="63%">
Creates a collection of addresses available for receiving ACD calls on this agent handler. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
 

 

