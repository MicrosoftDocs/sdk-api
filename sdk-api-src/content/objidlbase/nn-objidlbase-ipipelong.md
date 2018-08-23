---
UID: NN:objidlbase.IPipeLong
title: IPipeLong
author: windows-sdk-content
description: Transfers data of the long integer type (which is 32 bits wide).
old-location: com\ipipelong.htm
old-project: com
ms.assetid: c1b4d3b3-e1bf-4441-8cea-b667b82c4c27
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPipeLong, IPipeLong interface [COM], IPipeLong interface [COM],described, _com_ipipelong, com.ipipelong, objidlbase/IPipeLong
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IPipeLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPipeLong interface


## -description


Transfers data of the long integer type (which is 32 bits wide). 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPipeLong</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IPipeLong</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPipeLong</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33da8bd7-3350-4f6e-84f8-3046da226d2f">Pull</a>
</td>
<td align="left" width="63%">
Retrieves data of the long integer type from the pipe source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16389e32-74f9-419b-bcc5-63fe43b3e456">Push</a>
</td>
<td align="left" width="63%">
Sends data of the long integer type to the pipe source.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>, <a href="https://msdn.microsoft.com/434d0e0e-55a0-4a08-bc63-ebca4b2bdcca">IPipeDouble</a>, and <b>IPipeLong</b> interfaces are similar to the standard DCE/RPC pipes. However, the COM implementation of pipes offers more flexibility. With the COM implementation, the basic idea is that the pipe is simply another interface with two methods: <a href="https://msdn.microsoft.com/33da8bd7-3350-4f6e-84f8-3046da226d2f">Pull</a> and <a href="https://msdn.microsoft.com/16389e32-74f9-419b-bcc5-63fe43b3e456">Push</a>. This results in three main benefits: 



<ul>
<li>A COM pipe is another interface, so it can be received as an out parameter from a method call and then either <a href="https://msdn.microsoft.com/33da8bd7-3350-4f6e-84f8-3046da226d2f">Pull</a> or <a href="https://msdn.microsoft.com/16389e32-74f9-419b-bcc5-63fe43b3e456">Push</a> can be called. </li>
<li>There are no restrictions on when to call the <a href="https://msdn.microsoft.com/33da8bd7-3350-4f6e-84f8-3046da226d2f">Pull</a> and <a href="https://msdn.microsoft.com/16389e32-74f9-419b-bcc5-63fe43b3e456">Push</a> methods, so a pipe is in reality bidirectional. 
</li>
<li>Pipes are interfaces, so the method calls can be asynchronous and follow those rules.</li>
</ul>
For more information, see <a href="https://msdn.microsoft.com/913d5e2a-00ad-4060-9274-a6db23fb2817">Pipes</a> in the RPC documentation.




## -see-also




<a href="https://msdn.microsoft.com/e3e01280-c015-488a-8be4-9740c44c0041">IPipeByte</a>



<a href="https://msdn.microsoft.com/434d0e0e-55a0-4a08-bc63-ebca4b2bdcca">IPipeDouble</a>
 

 

