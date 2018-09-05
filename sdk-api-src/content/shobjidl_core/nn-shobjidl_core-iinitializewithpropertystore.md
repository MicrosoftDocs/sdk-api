---
UID: NN:shobjidl_core.IInitializeWithPropertyStore
title: IInitializeWithPropertyStore
author: windows-sdk-content
description: Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a property store.
old-location: shell\IInitializeWithPropertyStore.htm
old-project: shell
ms.assetid: da8592a9-7727-433f-ac92-abf22a735eb2
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IInitializeWithPropertyStore, IInitializeWithPropertyStore interface [Windows Shell], IInitializeWithPropertyStore interface [Windows Shell],described, _shell_IInitializeWithPropertyStore, shell.IInitializeWithPropertyStore, shobjidl_core/IInitializeWithPropertyStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithPropertyStore
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInitializeWithPropertyStore interface


## -description


Exposes a method that initializes a handler, such as a property handler, thumbnail handler, or preview handler, with a property store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitializeWithPropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitializeWithPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitializeWithPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6890873f-d929-42a1-ab75-6f408581d74f">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a handler with an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Use this interface when initializing a handler for OpenSearch result sets, which are returned as RSS or Atom feeds.




## -see-also




<a href="https://msdn.microsoft.com/da8592a9-7727-433f-ac92-abf22a735eb2">IInitializeWithPropertyStore</a>



<a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a>
 

 

