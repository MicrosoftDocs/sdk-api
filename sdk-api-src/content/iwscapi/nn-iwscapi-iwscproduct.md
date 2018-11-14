---
UID: NN:iwscapi.IWscProduct
title: IWscProduct
author: windows-sdk-content
description: Provides methods for getting product information for an individual provider to interact with Windows Security Center.
old-location: winprog\iwscproduct.htm
tech.root: devnotes
ms.assetid: C637E67A-CED7-4235-AAF3-22730E9C7E91
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IWscProduct, IWscProduct interface [Windows API], IWscProduct interface [Windows API],described, iwscapi/IWscProduct, winprog.iwscproduct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWscProduct interface


## -description


Provides methods for getting product information for an individual provider to interact with Windows Security Center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWscProduct</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWscProduct</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5270D8AF-AA69-4CC8-8ABC-F0716B3ED588">ProductName</a>
</td>
<td align="left" width="63%">
Returns the current product information for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73E4EA93-C298-4F25-BC51-DB6E38B48EE3">ProductState</a>
</td>
<td align="left" width="63%">
Returns the current state of the signature data for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3BE70437-8BBE-47DF-8C5E-390353073580">ProductStateTimeStamp</a>
</td>
<td align="left" width="63%">
Returns the current time  stamp for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6922B572-4E00-4B0B-BE1F-64343DD776A0">RemediationPath</a>
</td>
<td align="left" width="63%">
Returns the current remediation path for the security product.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07F7EADE-44E9-472F-BA30-7B7EDEF48192">SignatureStatus</a>
</td>
<td align="left" width="63%">
Returns the current status of the signature data for the security product.

</td>
</tr>
</table> 

