---
UID: NN:wsddisco.IWSDScopeMatchingRule
title: IWSDScopeMatchingRule
author: windows-driver-content
description: Is implemented by the client program to supply a custom scope matching rule which can be used to extend the standard scope matching rules defined in WS-Discovery.
old-location: ncd\iwsdscopematchingrule.htm
old-project: WsdApi
ms.assetid: c608215d-6c72-4567-bf81-15af665e8c52
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDScopeMatchingRule, IWSDScopeMatchingRule interface, IWSDScopeMatchingRule interface,described, ncd.iwsdscopematchingrule, wsddisco/IWSDScopeMatchingRule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDScopeMatchingRule
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDScopeMatchingRule interface


## -description


Is implemented by the client program to supply a custom scope matching rule which can be used to extend the standard scope matching rules defined in WS-Discovery.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDScopeMatchingRule</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDScopeMatchingRule</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/86ce14eb-555f-4575-a335-8a428cffa20d">GetScopeRule</a>
</td>
<td align="left" width="63%">
Called to return a URI defining the implemented scope matching rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0790d3ef-c84a-4882-96f6-dbca87b2ec53">MatchScopes</a>
</td>
<td align="left" width="63%">
Called to compare two scopes to determine if they match.

</td>
</tr>
</table> 

