---
UID: NN:wmp.IWMPError
title: IWMPError
author: windows-sdk-content
description: The IWMPError interface provides methods for accessing a collection of IWMPErrorItem pointers.
old-location: wmp\iwmperror.htm
tech.root: WMP
ms.assetid: f22759cd-0ca7-4992-bb17-0272b35d6d75
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPError, IWMPError interface [Windows Media Player], IWMPError interface [Windows Media Player],described, IWMPErrorInterface, wmp.iwmperror, wmp/IWMPError
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPError</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPError</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8c965b48-d178-4b41-add7-0b7d208380a3">clearErrorQueue</a>
</td>
<td align="left" width="63%">
Clears the errors from the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ad21e08-4566-4f3a-8506-308432996481">get_errorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of errors in the error queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fda2f53-e8d8-4b67-9aa1-72273fc68f6c">get_item</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPErrorItem</b> interface at the given index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98ece2f3-36c4-4bb2-9a06-c3ce57cbcbe7">webHelp</a>
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
<a href="https://msdn.microsoft.com/24fbb34d-4a5e-4a00-85fc-9659a31dc650">IWMPCore</a>
</td>
<td>
<a href="https://msdn.microsoft.com/db00797b-989f-4f92-8fac-aaa147e37383">get_error</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4675eebf-80d7-4412-b3f1-ec54b977db31">IWMPErrorItem Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

