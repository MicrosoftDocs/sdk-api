---
UID: NN:ctxtcall.IContextCallback
title: IContextCallback
author: windows-driver-content
description: Provides a mechanism to execute a function inside a specific COM+ object context.
old-location: com\icontextcallback.htm
old-project: com
ms.assetid: 47af7b80-3419-4a40-8932-a5a27f297dc9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IContextCallback, IContextCallback interface [COM], IContextCallback interface [COM],described, _com_icontextcallback, com.icontextcallback, ctxtcall/IContextCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctxtcall.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_LBBALLOONINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ctxtcall.h
api_name:
-	IContextCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IContextCallback interface


## -description


Provides a mechanism to execute a function inside a specific COM+ object context.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextCallback</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IContextCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7446792e-7f29-4ad4-8245-b86f63f2df18">ContextCallback</a>
</td>
<td align="left" width="63%">
Enters the object context, executes the specified function, and returns.

</td>
</tr>
</table> 


## -remarks



 An instance of this interface for the current context can be obtained using <a href="https://msdn.microsoft.com/97a0c6c3-a011-44dc-b428-aabdad7d4364">CoGetObjectContext</a>.



