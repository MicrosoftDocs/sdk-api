---
UID: NN:azroles.IAzBizRuleParameters
title: IAzBizRuleParameters (azroles.h)
description: Provides methods and properties used to manage a list of parameters that can be passed to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters.htm
tech.root: SecAuthZ
ms.assetid: 07eb33be-71a3-42fc-b7f3-12be23746aa3
ms.date: 12/05/2018
ms.keywords: IAzBizRuleParameters, IAzBizRuleParameters interface [Security], IAzBizRuleParameters interface [Security],described, azroles/IAzBizRuleParameters, security.iazbizruleparameters
f1_keywords:
- azroles/IAzBizRuleParameters
dev_langs:
- c++
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Azroles.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzBizRuleParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzBizRuleParameters interface


## -description


The <b>IAzBizRuleParameters</b> interface provides methods and properties used to manage a list of parameters that can be passed to business rule (BizRule) scripts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleParameters</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IAzBizRuleParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzBizRuleParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-addparameter">AddParameter</a>
</td>
<td align="left" width="63%">
Adds a parameter to the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-addparameters">AddParameters</a>
</td>
<td align="left" width="63%">
Adds  parameters to the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-getparametervalue">GetParameterValue</a>
</td>
<td align="left" width="63%">
Gets the value type of the BizRule parameter with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified parameter from the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all parameters from the list of parameters available to BizRule scripts.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleParameters</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizruleparameters-get_count">Count</a>


</td>
<td align="left" width="63%">
Gets the number of parameters available to BizRule scripts.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext3-get_bizruleparameters">IAzClientContext3::BizRuleParameters</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

