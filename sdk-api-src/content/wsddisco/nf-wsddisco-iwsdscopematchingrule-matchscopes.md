---
UID: NF:wsddisco.IWSDScopeMatchingRule.MatchScopes
title: IWSDScopeMatchingRule::MatchScopes (wsddisco.h)
description: Is called to compare two scopes to determine if they match.
helpviewer_keywords: ["IWSDScopeMatchingRule interface","MatchScopes method","IWSDScopeMatchingRule.MatchScopes","IWSDScopeMatchingRule::MatchScopes","MatchScopes","MatchScopes method","MatchScopes method","IWSDScopeMatchingRule interface","ncd.iwsdscopematchingrule_matchscopes_method","wsddisco/IWSDScopeMatchingRule::MatchScopes"]
old-location: ncd\iwsdscopematchingrule_matchscopes_method.htm
tech.root: ncd
ms.assetid: 0790d3ef-c84a-4882-96f6-dbca87b2ec53
ms.date: 12/05/2018
ms.keywords: IWSDScopeMatchingRule interface,MatchScopes method, IWSDScopeMatchingRule.MatchScopes, IWSDScopeMatchingRule::MatchScopes, MatchScopes, MatchScopes method, MatchScopes method,IWSDScopeMatchingRule interface, ncd.iwsdscopematchingrule_matchscopes_method, wsddisco/IWSDScopeMatchingRule::MatchScopes
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
 - IWSDScopeMatchingRule::MatchScopes
 - wsddisco/IWSDScopeMatchingRule::MatchScopes
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
 - IWSDScopeMatchingRule.MatchScopes
---

# IWSDScopeMatchingRule::MatchScopes


## -description

Is called to compare two scopes to determine if they match.

## -parameters

### -param pszScope1 [in]

Pointer to the first scope matching rule.

### -param pszScope2 [in]

Pointer to the second scope matching rule.

### -param pfMatch [out]

Set to <b>TRUE</b> if the scopes received via <i>pszScope1</i> and <i>pszScope2</i> match, <b>FALSE</b> otherwise.

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

<b>MatchScopes</b> will be called on custom scope matching rules to determine whether or not the two scopes provided match. <i>pfMatch</i> should be assigned either <b>TRUE</b> or <b>FALSE</b> to indicate the match status.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdscopematchingrule">IWSDScopeMatchingRule</a>