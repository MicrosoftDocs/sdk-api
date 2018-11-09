---
UID: NN:shobjidl_core.IInitializeWithItem
title: IInitializeWithItem
author: windows-sdk-content
description: Exposes a method used to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with an IShellItem.
old-location: shell\IInitializeWithItem.htm
tech.root: shell
ms.assetid: 95f3917e-66ca-45de-a3ed-811680a179e7
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IInitializeWithItem, IInitializeWithItem interface [Windows Shell], IInitializeWithItem interface [Windows Shell],described, shell.IInitializeWithItem, shell_IInitializeWithItem, shobjidl_core/IInitializeWithItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IInitializeWithItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeWithItem interface


## -description


Exposes a method used to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitializeWithItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeWithItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61abf5c8-2847-4788-9d99-65f3b1c821d6">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a handler with an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>.

</td>
</tr>
</table> 


## -remarks



Whenever possible, it is recommended that initialization be done through a stream using <a href="https://msdn.microsoft.com/9050845d-1e70-4e85-8d2f-c8bbb382abe5">IInitializeWithStream</a>. Benefits of this include increased security and stability.



