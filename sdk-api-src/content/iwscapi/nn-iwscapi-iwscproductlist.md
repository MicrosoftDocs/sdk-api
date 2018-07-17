---
UID: NN:iwscapi.IWSCProductList
title: IWSCProductList
author: windows-sdk-content
description: Provides methods to collect product information for the selected type of providers installed on the computer.
old-location: winprog\iwscproductlist.htm
old-project: DevNotes
ms.assetid: 81BC78F1-6F95-49D3-8EDD-EB7E13119A86
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWSCProductList, IWSCProductList interface [Windows API], IWSCProductList interface [Windows API],described, iwscapi/IWSCProductList, winprog.iwscproductlist
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSC_SECURITY_SIGNATURE_STATUS
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
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>
</td>
<td align="left" width="63%">
Gathers the total number of all security product providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Gathers information on all of the providers of the specified type on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Returns one of the  types of providers on the computer.

</td>
</tr>
</table> 

