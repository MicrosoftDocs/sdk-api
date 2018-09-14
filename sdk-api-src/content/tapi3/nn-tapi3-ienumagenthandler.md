---
UID: NN:tapi3.IEnumAgentHandler
title: IEnumAgentHandler
author: windows-sdk-content
description: The IEnumAgentHandler interface provides COM-standard enumeration methods for the ITAgentHandler interface. The ITTAPICallCenter::EnumerateAgentHandlers method returns a pointer to IEnumAgentHandler.
old-location: tapi3\ienumagenthandler.htm
tech.root: TAPI
ms.assetid: a318318a-769e-4619-a461-4988d90d3f1a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IEnumAgentHandler, IEnumAgentHandler interface [TAPI 2.2], IEnumAgentHandler interface [TAPI 2.2],described, _tapi3_ienumagenthandler, tapi3.ienumagenthandler, tapi3cc/IEnumAgentHandler
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumAgentHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumAgentHandler interface


## -description


The 
<b>IEnumAgentHandler</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface. The 
<a href="https://msdn.microsoft.com/5bd0a926-0d99-4efe-a995-28654c97c97a">ITTAPICallCenter::EnumerateAgentHandlers</a> method returns a pointer to 
<b>IEnumAgentHandler</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAgentHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumAgentHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAgentHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7358d0d-6d5a-4845-a212-d278a8d2b7fe">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e6a7db0-c339-4a36-aea8-e3f9f2d5cd09">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb113db5-718d-4c5e-92ad-4eb605911c71">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf6b7003-13f1-4203-b341-2c9796cffdd2">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

