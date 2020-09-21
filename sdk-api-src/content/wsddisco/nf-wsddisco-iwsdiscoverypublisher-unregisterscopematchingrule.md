---
UID: NF:wsddisco.IWSDiscoveryPublisher.UnRegisterScopeMatchingRule
title: IWSDiscoveryPublisher::UnRegisterScopeMatchingRule (wsddisco.h)
description: Removes support for a custom scope matching rule.
helpviewer_keywords: ["IWSDiscoveryPublisher interface","UnRegisterScopeMatchingRule method","IWSDiscoveryPublisher.UnRegisterScopeMatchingRule","IWSDiscoveryPublisher::UnRegisterScopeMatchingRule","UnRegisterScopeMatchingRule","UnRegisterScopeMatchingRule method","UnRegisterScopeMatchingRule method","IWSDiscoveryPublisher interface","ncd.iwsdiscoverypublisher_unregisterscopematchingrule_method","wsddisco/IWSDiscoveryPublisher::UnRegisterScopeMatchingRule"]
old-location: ncd\iwsdiscoverypublisher_unregisterscopematchingrule_method.htm
tech.root: ncd
ms.assetid: 82af2ea1-8415-45f7-ab05-805a66689482
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,UnRegisterScopeMatchingRule method, IWSDiscoveryPublisher.UnRegisterScopeMatchingRule, IWSDiscoveryPublisher::UnRegisterScopeMatchingRule, UnRegisterScopeMatchingRule, UnRegisterScopeMatchingRule method, UnRegisterScopeMatchingRule method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_unregisterscopematchingrule_method, wsddisco/IWSDiscoveryPublisher::UnRegisterScopeMatchingRule
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
 - IWSDiscoveryPublisher::UnRegisterScopeMatchingRule
 - wsddisco/IWSDiscoveryPublisher::UnRegisterScopeMatchingRule
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
 - IWSDiscoveryPublisher.UnRegisterScopeMatchingRule
---

# IWSDiscoveryPublisher::UnRegisterScopeMatchingRule


## -description

Removes support for a custom scope matching rule.

## -parameters

### -param pScopeMatchingRule [in]

Pointer to an <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdscopematchingrule">IWSDScopeMatchingRule</a> object that represents a custom scope matching rule.

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
</table>

## -remarks

<b>UnRegisterScopeMatchingRule</b> removes a previously associated custom scope matching rule.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>