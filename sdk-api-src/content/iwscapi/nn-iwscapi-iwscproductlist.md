---
UID: NN:iwscapi.IWSCProductList
title: IWSCProductList (iwscapi.h)
description: Provides methods to collect product information for the selected type of providers installed on the computer.
helpviewer_keywords: ["IWSCProductList","IWSCProductList interface [Windows API]","IWSCProductList interface [Windows API]","described","iwscapi/IWSCProductList","winprog.iwscproductlist"]
old-location: winprog\iwscproductlist.htm
tech.root: winprog
ms.assetid: 81BC78F1-6F95-49D3-8EDD-EB7E13119A86
ms.date: 12/05/2018
ms.keywords: IWSCProductList, IWSCProductList interface [Windows API], IWSCProductList interface [Windows API],described, iwscapi/IWSCProductList, winprog.iwscproductlist
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
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSCProductList
 - iwscapi/IWSCProductList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - iwscapi.h
api_name:
 - IWSCProductList
---

# IWSCProductList interface


## -description

Provides methods  to collect product information for the selected type of providers installed on the computer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSCProductList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSCProductList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSCProductList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwscapi/nf-iwscapi-iwscproductlist-get_count">Count</a>
</td>
<td align="left" width="63%">
Gathers the total number of all security product providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwscapi/nf-iwscapi-iwscproductlist-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Gathers information on all of the providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iwscapi/nf-iwscapi-iwscproductlist-get_item">Item</a>
</td>
<td align="left" width="63%">
Returns one of the  types of providers on the computer.

</td>
</tr>
</table>