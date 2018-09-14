---
UID: NN:shobjidl_core.IAssocHandlerInvoker
title: IAssocHandlerInvoker
author: windows-sdk-content
description: Exposes methods that invoke an associated application handler.
old-location: shell\IAssocHandlerInvoker.htm
tech.root: shell
ms.assetid: b602280e-4237-4539-9a10-cec21c65e90d
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IAssocHandlerInvoker, IAssocHandlerInvoker interface [Windows Shell], IAssocHandlerInvoker interface [Windows Shell],described, _shell_IAssocHandlerInvoker, shell.IAssocHandlerInvoker, shobjidl_core/IAssocHandlerInvoker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IAssocHandlerInvoker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssocHandlerInvoker interface


## -description


Exposes methods that invoke an associated application handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssocHandlerInvoker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAssocHandlerInvoker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssocHandlerInvoker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5de945-b177-4cbc-817c-447b2174323e">Invoke</a>
</td>
<td align="left" width="63%">
Invokes an associated application handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4000557-2a89-494c-8b0e-c67a2e2c4445">SupportsSelection</a>
</td>
<td align="left" width="63%">
Determines whether an invoker supports its selection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/c8b11157-4d00-4ab1-aea5-ce8ae35c43ce">IEnumAssocHandlers</a>



<a href="https://msdn.microsoft.com/83db466b-e00c-4015-879f-c5c222f45b8c">SHAssocEnumHandlers</a>
 

 

