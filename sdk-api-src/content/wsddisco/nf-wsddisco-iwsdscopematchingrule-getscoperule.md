---
UID: NF:wsddisco.IWSDScopeMatchingRule.GetScopeRule
title: IWSDScopeMatchingRule::GetScopeRule (wsddisco.h)
description: Is called to return a URI defining the implemented scope matching rule.
helpviewer_keywords: ["GetScopeRule","GetScopeRule method","GetScopeRule method","IWSDScopeMatchingRule interface","IWSDScopeMatchingRule interface","GetScopeRule method","IWSDScopeMatchingRule.GetScopeRule","IWSDScopeMatchingRule::GetScopeRule","ncd.iwsdscopematchingrule_getscoperule_method","wsddisco/IWSDScopeMatchingRule::GetScopeRule"]
old-location: ncd\iwsdscopematchingrule_getscoperule_method.htm
tech.root: ncd
ms.assetid: 86ce14eb-555f-4575-a335-8a428cffa20d
ms.date: 12/05/2018
ms.keywords: GetScopeRule, GetScopeRule method, GetScopeRule method,IWSDScopeMatchingRule interface, IWSDScopeMatchingRule interface,GetScopeRule method, IWSDScopeMatchingRule.GetScopeRule, IWSDScopeMatchingRule::GetScopeRule, ncd.iwsdscopematchingrule_getscoperule_method, wsddisco/IWSDScopeMatchingRule::GetScopeRule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDScopeMatchingRule::GetScopeRule
 - wsddisco/IWSDScopeMatchingRule::GetScopeRule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDScopeMatchingRule.GetScopeRule
---

# IWSDScopeMatchingRule::GetScopeRule


## -description

Is called to return a URI defining the implemented scope matching rule.

## -parameters

### -param ppszScopeMatchingRule [out]

Pointer to the scope matching rule. The implementer must allocate memory using <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdallocatelinkedmemory">WSDAllocateLinkedMemory</a> and the caller must release memory using <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.

## -returns

Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
</table>

## -remarks

<b>GetScopeRule</b> should provide a copy of the URI for the scope matching rule this object represents. The copy will be released by the caller using <a href="/windows/desktop/api/wsdutil/nf-wsdutil-wsdfreelinkedmemory">WSDFreeLinkedMemory</a>.

<i>ppszScopeMatchingRule</i> should never be <b>NULL</b> or an empty string. To register for the <b>NULL</b> scope matching rule, register for the RFC2396 rule as defined in <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery</a>. Probe messages containing a <b>NULL</b> MatchBy value will be converted to RFC2396 before <b>GetScopeRule</b> is called.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdscopematchingrule">IWSDScopeMatchingRule</a>