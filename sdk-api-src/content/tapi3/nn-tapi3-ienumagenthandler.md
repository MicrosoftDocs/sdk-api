---
UID: NN:tapi3.IEnumAgentHandler
title: IEnumAgentHandler (tapi3.h)
author: windows-sdk-content
description: The IEnumAgentHandler interface provides COM-standard enumeration methods for the ITAgentHandler interface. The ITTAPICallCenter::EnumerateAgentHandlers method returns a pointer to IEnumAgentHandler.
old-location: tapi3\ienumagenthandler.htm
tech.root: Tapi
ms.assetid: a318318a-769e-4619-a461-4988d90d3f1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumAgentHandler, IEnumAgentHandler interface [TAPI 2.2], IEnumAgentHandler interface [TAPI 2.2],described, _tapi3_ienumagenthandler, tapi3.ienumagenthandler, tapi3cc/IEnumAgentHandler
ms.topic: interface
f1_keywords: 
 - "tapi3/IEnumAgentHandler"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAgentHandler interface


## -description


The 
<b>IEnumAgentHandler</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ittapicallcenter-enumerateagenthandlers">ITTAPICallCenter::EnumerateAgentHandlers</a> method returns a pointer to 
<b>IEnumAgentHandler</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAgentHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAgentHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumagenthandler-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

