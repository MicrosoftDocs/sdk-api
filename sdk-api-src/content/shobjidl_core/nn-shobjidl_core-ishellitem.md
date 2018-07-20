---
UID: NN:shobjidl_core.IShellItem
title: IShellItem
author: windows-sdk-content
description: Exposes methods that retrieve information about a Shell item. IShellItem and IShellItem2 are the preferred representations of items in any new code.
old-location: shell\IShellItem.htm
old-project: shell
ms.assetid: 599b9c0a-df04-4dbd-a5a6-a8736eecc560
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IShellItem, IShellItem interface [Windows Shell], IShellItem interface [Windows Shell],described, _win32_IShellItem, shell.IShellItem, shobjidl_core/IShellItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Shell32.dll
api_name:
 - IShellItem
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellItem interface


## -description


Exposes methods that retrieve information about a Shell item. <b>IShellItem</b> and <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a> are the preferred representations of items in any new code.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fadd70cd-5018-4b71-af7b-d9c780ebddc5">BindToHandler</a>
</td>
<td align="left" width="63%">
Binds to a handler for an item as specified by the handler ID value (BHID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406436">Compare</a>
</td>
<td align="left" width="63%">
Compares two <b>IShellItem</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8d48b4b-979e-48ed-9e57-279fd6fad5cc">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets a requested set of attributes of the <b>IShellItem</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b159be9-3797-4c8b-90f8-9d3b3a3afb71">GetDisplayName</a>
</td>
<td align="left" width="63%">
Gets the display name of the <b>IShellItem</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d62123af-2ae2-40f2-8581-c95b18491f20">GetParent</a>
</td>
<td align="left" width="63%">
Gets the parent of an <b>IShellItem</b> object.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Third parties do not implement this interface; only use the implementation provided with the system.




## -see-also




<a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>
 

 

