---
UID: NN:wmp.IWMPError
title: IWMPError (wmp.h)
author: windows-sdk-content
description: The IWMPError interface provides methods for accessing a collection of IWMPErrorItem pointers.
old-location: wmp\iwmperror.htm
tech.root: WMP
ms.assetid: f22759cd-0ca7-4992-bb17-0272b35d6d75
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPError, IWMPError interface [Windows Media Player], IWMPError interface [Windows Media Player],described, IWMPErrorInterface, wmp.iwmperror, wmp/IWMPError
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
 - IWMPError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPError interface


## -description



The <b>IWMPError</b> interface provides methods for accessing a collection of <b>IWMPErrorItem</b> pointers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPError</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563283(v=VS.85).aspx">clearErrorQueue</a>
</td>
<td align="left" width="63%">
Clears the errors from the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563284(v=VS.85).aspx">get_errorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of errors in the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563285(v=VS.85).aspx">get_item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPErrorItem</b> interface at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563287(v=VS.85).aspx">webHelp</a>
</td>
<td align="left" width="63%">
Launches the Microsoft Windows Media Player Web Help page to display further information about the error.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPError</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563216(v=VS.85).aspx">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563229(v=VS.85).aspx">get_error</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563273(v=VS.85).aspx">IWMPErrorItem Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

