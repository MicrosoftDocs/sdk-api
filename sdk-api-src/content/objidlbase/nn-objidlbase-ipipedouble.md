---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPipeDouble interface


## -description


Transfers data of the double type (which is 64 bits wide). 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPipeDouble</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPipeDouble</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPipeDouble</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/393e44fa-48fe-4a8d-b337-9b875129a502">Pull</a>
</td>
<td align="left" width="63%">
Retrieves data of the double integer type from the pipe source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49c9121f-eb92-42e4-bd30-fe2213d44de9">Push</a>
</td>
<td align="left" width="63%">
Sends data of the double integer type to the pipe source.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>, <b>IPipeDouble</b>, and <a href="https://msdn.microsoft.com/c1b4d3b3-e1bf-4441-8cea-b667b82c4c27">IPipeLong</a> interfaces are similar to the standard DCE/RPC pipes. However, the COM implementation of pipes offers more flexibility. With the COM implementation, the basic idea is that the pipe is simply another interface with two methods: <a href="https://msdn.microsoft.com/393e44fa-48fe-4a8d-b337-9b875129a502">Pull</a> and <a href="https://msdn.microsoft.com/49c9121f-eb92-42e4-bd30-fe2213d44de9">Push</a>. This results in three main benefits: 



<ul>
<li>A COM pipe is another interface, so it can be received as an out parameter from a method call and then either <a href="https://msdn.microsoft.com/393e44fa-48fe-4a8d-b337-9b875129a502">Pull</a> or <a href="https://msdn.microsoft.com/49c9121f-eb92-42e4-bd30-fe2213d44de9">Push</a> can be called. </li>
<li>There are no restrictions on when to call the <a href="https://msdn.microsoft.com/393e44fa-48fe-4a8d-b337-9b875129a502">Pull</a> and <a href="https://msdn.microsoft.com/49c9121f-eb92-42e4-bd30-fe2213d44de9">Push</a> methods, so a pipe is in reality bidirectional. 
</li>
<li>Pipes are interfaces, so the method calls can be asynchronous and follow those rules.</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/913d5e2a-00ad-4060-9274-a6db23fb2817">Pipes</a> in the RPC documentation.




## -see-also




<a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>



<a href="https://msdn.microsoft.com/c1b4d3b3-e1bf-4441-8cea-b667b82c4c27">IPipeLong</a>
 

 

