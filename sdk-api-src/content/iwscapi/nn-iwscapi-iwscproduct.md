---
UID: NN:iwscapi.IWscProduct
title: IWscProduct (iwscapi.h)
description: Provides methods for getting product information for an individual provider to interact with Windows Security Center.
helpviewer_keywords: ["IWscProduct","IWscProduct interface [Windows API]","IWscProduct interface [Windows API]","described","iwscapi/IWscProduct","winprog.iwscproduct"]
old-location: winprog\iwscproduct.htm
tech.root: winprog
ms.assetid: C637E67A-CED7-4235-AAF3-22730E9C7E91
ms.date: 12/05/2018
ms.keywords: IWscProduct, IWscProduct interface [Windows API], IWscProduct interface [Windows API],described, iwscapi/IWscProduct, winprog.iwscproduct
f1_keywords:
- iwscapi/IWscProduct
dev_langs:
- c++
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wsccapi.lib
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsccapi.lib
api_name:
- IWscProduct
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWscProduct interface


## -description


Provides methods for getting product information for an individual provider to interact with Windows Security Center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWscProduct</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWscProduct</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWscProduct</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nf-iwscapi-iwscproduct-get_productname">ProductName</a>
</td>
<td align="left" width="63%">
Returns the current product information for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nf-iwscapi-iwscproduct-get_productstate">ProductState</a>
</td>
<td align="left" width="63%">
Returns the current state of the signature data for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nf-iwscapi-iwscproduct-get_productstatetimestamp">ProductStateTimeStamp</a>
</td>
<td align="left" width="63%">
Returns the current time  stamp for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nf-iwscapi-iwscproduct-get_remediationpath">RemediationPath</a>
</td>
<td align="left" width="63%">
Returns the current remediation path for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nf-iwscapi-iwscproduct-get_signaturestatus">SignatureStatus</a>
</td>
<td align="left" width="63%">
Returns the current status of the signature data for the security product.

</td>
</tr>
</table> 

