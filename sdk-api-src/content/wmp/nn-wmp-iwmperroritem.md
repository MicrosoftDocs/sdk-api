---
UID: NN:wmp.IWMPErrorItem
title: IWMPErrorItem (wmp.h)
author: windows-sdk-content
description: The IWMPErrorItem interface provides a way to access error information.
old-location: wmp\iwmperroritem.htm
tech.root: WMP
ms.assetid: 4675eebf-80d7-4412-b3f1-ec54b977db31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPErrorItem, IWMPErrorItem interface [Windows Media Player], IWMPErrorItem interface [Windows Media Player],described, IWMPErrorItemInterface, wmp.iwmperroritem, wmp/IWMPErrorItem
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
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563277(v=VS.85).aspx">get_customUrl</a>
</td>
<td align="left" width="63%">
Retrieves the URL of a website that displays specific information about codec download failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563278(v=VS.85).aspx">get_errorCode</a>
</td>
<td align="left" width="63%">
Retrieves the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563279(v=VS.85).aspx">get_errorContext</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the context of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563280(v=VS.85).aspx">get_errorDescription</a>
</td>
<td align="left" width="63%">
Retrieves a description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563281(v=VS.85).aspx">get_remedy</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563272(v=VS.85).aspx">IWMPError</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563285(v=VS.85).aspx">get_item</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563274(v=VS.85).aspx">IWMPErrorItem2 Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

