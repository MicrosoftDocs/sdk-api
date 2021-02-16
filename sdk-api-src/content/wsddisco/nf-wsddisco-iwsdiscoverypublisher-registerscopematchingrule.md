---
UID: NF:wsddisco.IWSDiscoveryPublisher.RegisterScopeMatchingRule
title: IWSDiscoveryPublisher::RegisterScopeMatchingRule (wsddisco.h)
description: Adds support for a custom scope matching rule.
helpviewer_keywords: ["IWSDiscoveryPublisher interface","RegisterScopeMatchingRule method","IWSDiscoveryPublisher.RegisterScopeMatchingRule","IWSDiscoveryPublisher::RegisterScopeMatchingRule","RegisterScopeMatchingRule","RegisterScopeMatchingRule method","RegisterScopeMatchingRule method","IWSDiscoveryPublisher interface","ncd.iwsdiscoverypublisher_registerscopematchingrule_method","wsddisco/IWSDiscoveryPublisher::RegisterScopeMatchingRule"]
old-location: ncd\iwsdiscoverypublisher_registerscopematchingrule_method.htm
tech.root: ncd
ms.assetid: 3ceb55de-c8be-43a7-93d7-8f674f9645ef
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,RegisterScopeMatchingRule method, IWSDiscoveryPublisher.RegisterScopeMatchingRule, IWSDiscoveryPublisher::RegisterScopeMatchingRule, RegisterScopeMatchingRule, RegisterScopeMatchingRule method, RegisterScopeMatchingRule method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_registerscopematchingrule_method, wsddisco/IWSDiscoveryPublisher::RegisterScopeMatchingRule
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
 - IWSDiscoveryPublisher::RegisterScopeMatchingRule
 - wsddisco/IWSDiscoveryPublisher::RegisterScopeMatchingRule
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
 - IWSDiscoveryPublisher.RegisterScopeMatchingRule
---

# IWSDiscoveryPublisher::RegisterScopeMatchingRule


## -description

Adds support for a custom scope matching rule.

## -parameters

### -param pScopeMatchingRule [in]

Pointer to an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdscopematchingrule">IWSDScopeMatchingRule</a> object that represents a  custom scope matching rule.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pScopeMatchingRule</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

<b>RegisterScopeMatchingRule</b> allows custom scope matching rules to be defined and added to the existing set defined in the <a href="https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf">WS-Discovery specification</a>.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>