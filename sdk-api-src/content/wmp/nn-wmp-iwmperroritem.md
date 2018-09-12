---
UID: NN:wmp.IWMPErrorItem
title: IWMPErrorItem
author: windows-sdk-content
description: The IWMPErrorItem interface provides a way to access error information.
old-location: wmp\iwmperroritem.htm
tech.root: WMP
ms.assetid: 4675eebf-80d7-4412-b3f1-ec54b977db31
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPErrorItem, IWMPErrorItem interface [Windows Media Player], IWMPErrorItem interface [Windows Media Player],described, IWMPErrorItemInterface, wmp.iwmperroritem, wmp/IWMPErrorItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - wmp.h
api_name:
 - IWMPErrorItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPErrorItem interface


## -description



The <b>IWMPErrorItem</b> interface provides a way to access error information.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPErrorItem</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPErrorItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPErrorItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cf54c10-a06d-49fc-aa8e-e6264ce23061">get_customUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL of a website that displays specific information about codec download failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e809a1bf-1c7e-4006-9d27-e9921f2f14b2">get_errorCode</a>
</td>
<td align="left" width="63%">
Retrieves the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/575f14e7-7a5b-4000-9957-253c40b1ef62">get_errorContext</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the context of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb322580-2cc6-4094-9da3-9b8d78a5cb48">get_errorDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f37ec43a-cf58-4e90-9b2a-aef8afc30744">get_remedy</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPErrorItem</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f22759cd-0ca7-4992-bb17-0272b35d6d75">IWMPError</a>
</td>
<td>
<a href="https://msdn.microsoft.com/6fda2f53-e8d8-4b67-9aa1-72273fc68f6c">get_item</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b71d06db-c9bc-44fc-9e23-a16f89c56c1c">IWMPErrorItem2 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

