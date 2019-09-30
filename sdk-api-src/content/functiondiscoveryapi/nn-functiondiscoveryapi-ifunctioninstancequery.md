---
UID: NN:functiondiscoveryapi.IFunctionInstanceQuery
title: IFunctionInstanceQuery (functiondiscoveryapi.h)
author: windows-sdk-content
description: Implements the asynchronous query for a function instance based on category and subcategory.
old-location: ncd\ifunctioninstancequery.htm
tech.root: FunDisc
ms.assetid: 03343d85-c0db-436d-bedc-c001b1886173
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionInstanceQuery, IFunctionInstanceQuery interface, IFunctionInstanceQuery interface,described, functiondiscoveryapi/IFunctionInstanceQuery, ncd.ifunctioninstancequery
ms.topic: interface
f1_keywords: 
 - "functiondiscoveryapi/IFunctionInstanceQuery"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionInstanceQuery interface


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

This interface implements the asynchronous query for a function instance based on category and subcategory. A pointer to this interface is returned when the query is created by the client program.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFunctionInstanceQuery</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFunctionInstanceQuery</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancequery-execute">Execute</a>
</td>
<td align="left" width="63%">
Performs the query defined by <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscovery-createinstancequery">CreateInstanceQuery</a>.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancequery-execute">Execute</a> method must be invoked by the client program before any data can be retrieved from the query object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fundisc/function-discovery-queries">Function Discovery Queries</a>
 

 

