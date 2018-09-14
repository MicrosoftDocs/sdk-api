---
UID: NN:functiondiscoveryapi.IFunctionInstanceQuery
title: IFunctionInstanceQuery
author: windows-sdk-content
description: Implements the asynchronous query for a function instance based on category and subcategory.
old-location: ncd\ifunctioninstancequery.htm
tech.root: fundisc
ms.assetid: 03343d85-c0db-436d-bedc-c001b1886173
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IFunctionInstanceQuery, IFunctionInstanceQuery interface, IFunctionInstanceQuery interface,described, functiondiscoveryapi/IFunctionInstanceQuery, ncd.ifunctioninstancequery
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionInstanceQuery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface implements the asynchronous query for a function instance based on category and subcategory. A pointer to this interface is returned when the query is created by the client program.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceQuery</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFunctionInstanceQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFunctionInstanceQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42618944-6ae6-45f0-85f9-3c958d719ed2">Execute</a>
</td>
<td align="left" width="63%">
Performs the query defined by <a href="https://msdn.microsoft.com/80e70972-ced1-416e-aa4f-69c54b2cbf95">CreateInstanceQuery</a>.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/42618944-6ae6-45f0-85f9-3c958d719ed2">Execute</a> method must be invoked by the client program before any data can be retrieved from the query object.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>
 

 

