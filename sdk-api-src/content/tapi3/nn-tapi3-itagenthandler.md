---
UID: NN:tapi3.ITAgentHandler
title: ITAgentHandler (tapi3.h)
author: windows-sdk-content
description: The ITAgentHandler interface provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups. The IEnumAgentHandler::Next and ITTapiCallCenter::get_AgentHandlers methods create the ITAgentHandler interface.
old-location: tapi3\itagenthandler.htm
tech.root: Tapi
ms.assetid: 11861d77-39ad-4d85-bf68-ba0f4321ba7c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITAgentHandler, ITAgentHandler interface [TAPI 2.2], ITAgentHandler interface [TAPI 2.2],described, _tapi3_itagenthandler, tapi3.itagenthandler, tapi3cc/ITAgentHandler
ms.topic: interface
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
 - ITAgentHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgentHandler interface


## -description


The 
<b>ITAgentHandler</b> interface provides methods to create Agent objects and enumerate Automatic Call Distribution (ACD) groups. The 
<a href="https://msdn.microsoft.com/0e6a7db0-c339-4a36-aea8-e3f9f2d5cd09">IEnumAgentHandler::Next</a> and 
<a href="https://msdn.microsoft.com/61972ea2-d3ab-4893-8fc6-cd3c10f8584e">ITTapiCallCenter::get_AgentHandlers</a> methods create the 
<b>ITAgentHandler</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAgentHandler</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f3242013-59a6-40f9-9bb1-0bc30f27311c">CreateAgent</a>
</td>
<td align="left" width="63%">
Creates an Agent object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c70e48-b990-47c7-a8b8-5fa3a84ec5ba">CreateAgentWithID</a>
</td>
<td align="left" width="63%">
Creates an Agent object based on an agent identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9078166-ff6a-4520-8209-e785bd6e7100">EnumerateACDGroups</a>
</td>
<td align="left" width="63%">
Enumerates ACD groups currently associated with the agent handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9821b073-c64b-4f2b-b771-6bf027f9aa70">EnumerateUsableAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses available for receiving ACD calls on this agent handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72dcc4c8-fac6-4635-995e-18a5693da99b">get_ACDGroups</a>
</td>
<td align="left" width="63%">
Creates a collection of ACD groups currently associated with the agent handler. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18596742-9a0e-44c1-97e1-1d13d84cc10c">get_Name</a>
</td>
<td align="left" width="63%">
Gets the agent handler name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee457b5c-e505-489c-93dc-8bdfb87c7afe">get_UsableAddresses</a>
</td>
<td align="left" width="63%">
Creates a collection of addresses available for receiving ACD calls on this agent handler. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>
 

 

