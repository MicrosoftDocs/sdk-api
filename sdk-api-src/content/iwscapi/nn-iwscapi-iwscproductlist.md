---
UID: NN:iwscapi.IWSCProductList
title: IWSCProductList
author: windows-sdk-content
description: Provides methods to collect product information for the selected type of providers installed on the computer.
old-location: winprog\iwscproductlist.htm
tech.root: devnotes
ms.assetid: 81BC78F1-6F95-49D3-8EDD-EB7E13119A86
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IWSCProductList, IWSCProductList interface [Windows API], IWSCProductList interface [Windows API],described, iwscapi/IWSCProductList, winprog.iwscproductlist
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
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - iwscapi.h
api_name:
 - IWSCProductList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSCProductList interface


## -description


Provides methods  to collect product information for the selected type of providers installed on the computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSCProductList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSCProductList</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A28A6D3B-DC11-418B-987F-04711358B6EE">Count</a>
</td>
<td align="left" width="63%">
Gathers the total number of all security product providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D003510-BCFE-45E9-A34E-58036C382157">Initialize</a>
</td>
<td align="left" width="63%">
Gathers information on all of the providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/041F45EF-BE1E-4C37-9BD7-ED9F45587ADA">Item</a>
</td>
<td align="left" width="63%">
Returns one of the  types of providers on the computer.

</td>
</tr>
</table> 

