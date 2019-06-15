---
UID: NN:azroles.IAzBizRuleContext
title: IAzBizRuleContext (azroles.h)
author: windows-sdk-content
description: Contains information about a Business Rule (BizRule) operation.
old-location: security\azbizrulecontext.htm
tech.root: SecAuthZ
ms.assetid: 664d0307-8915-4435-a6a3-3f464afd9029
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAzBizRuleContext, IAzBizRuleContext interface [Security], IAzBizRuleContext interface [Security],described, azroles/IAzBizRuleContext, security.azbizrulecontext
ms.topic: interface
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
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
 - IAzBizRuleContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzBizRuleContext interface


## -description


The <b>AzBizRuleContext</b> object contains information about a Business Rule (BizRule) operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAzBizRuleContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAzBizRuleContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-getparameter">GetParameter</a>
</td>
<td align="left" width="63%">
Gets the specified value from the <i>varParameterValues</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">IAzClientContext::AccessCheck</a> method.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAzBizRuleContext</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-put_businessruleresult">BusinessRuleResult</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Sets a value that indicates whether the BizRule allows the user to perform the requested task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazbizrulecontext-get_businessrulestring">BusinessRuleString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves an application-specific string for the BizRule.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">IAzClientContext::AccessCheck</a> method creates an <b>AzBizRuleContext</b> object before it calls a BizRule script.



