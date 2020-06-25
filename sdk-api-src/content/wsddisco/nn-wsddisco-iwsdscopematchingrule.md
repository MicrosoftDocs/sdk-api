---
UID: NN:wsddisco.IWSDScopeMatchingRule
title: IWSDScopeMatchingRule (wsddisco.h)
description: Is implemented by the client program to supply a custom scope matching rule which can be used to extend the standard scope matching rules defined in WS-Discovery.
helpviewer_keywords: ["IWSDScopeMatchingRule","IWSDScopeMatchingRule interface","IWSDScopeMatchingRule interface","described","ncd.iwsdscopematchingrule","wsddisco/IWSDScopeMatchingRule"]
old-location: ncd\iwsdscopematchingrule.htm
tech.root: WsdApi
ms.assetid: c608215d-6c72-4567-bf81-15af665e8c52
ms.date: 12/05/2018
ms.keywords: IWSDScopeMatchingRule, IWSDScopeMatchingRule interface, IWSDScopeMatchingRule interface,described, ncd.iwsdscopematchingrule, wsddisco/IWSDScopeMatchingRule
f1_keywords:
- wsddisco/IWSDScopeMatchingRule
dev_langs:
- c++
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsdapi.dll
api_name:
- IWSDScopeMatchingRule
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDScopeMatchingRule interface


## -description


Is implemented by the client program to supply a custom scope matching rule which can be used to extend the standard scope matching rules defined in WS-Discovery.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDScopeMatchingRule</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDScopeMatchingRule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDScopeMatchingRule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdscopematchingrule-getscoperule">GetScopeRule</a>
</td>
<td align="left" width="63%">
Called to return a URI defining the implemented scope matching rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-iwsdscopematchingrule-matchscopes">MatchScopes</a>
</td>
<td align="left" width="63%">
Called to compare two scopes to determine if they match.

</td>
</tr>
</table> 

