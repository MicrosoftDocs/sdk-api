---
UID: NN:azroles.IAzBizRuleParameters
title: IAzBizRuleParameters
author: windows-sdk-content
description: Provides methods and properties used to manage a list of parameters that can be passed to business rule (BizRule) scripts.
old-location: security\iazbizruleparameters.htm
old-project: secauthz
ms.assetid: 07eb33be-71a3-42fc-b7f3-12be23746aa3
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: IAzBizRuleParameters, IAzBizRuleParameters interface [Security], IAzBizRuleParameters interface [Security],described, azroles/IAzBizRuleParameters, security.iazbizruleparameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzBizRuleParameters
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzBizRuleParameters interface


## -description


The <b>IAzBizRuleParameters</b> interface provides methods and properties used to manage a list of parameters that can be passed to business rule (BizRule) scripts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleParameters</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IAzBizRuleParameters</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ea5c45d4-34c8-4d7c-a1b2-8f45574d9449">AddParameter</a>
</td>
<td align="left" width="63%">
Adds a parameter to the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebf336a9-a64a-4ded-b508-56491ebf48e2">AddParameters</a>
</td>
<td align="left" width="63%">
Adds  parameters to the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/210dc872-0879-4b4f-bdc3-cbb2208dafbe">GetParameterValue</a>
</td>
<td align="left" width="63%">
Gets the value type of the BizRule parameter with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified parameter from the list of parameters available to BizRule scripts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ec13e1b-6b83-4178-a5a5-b278fe7c8c3c">RemoveAll</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Gets the number of parameters available to BizRule scripts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/161f8a84-ee00-4f39-9997-a1e3d1c5b7a8">IAzClientContext3::BizRuleParameters</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

