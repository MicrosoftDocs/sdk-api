---
UID: NN:objidlbase.IContext
title: IContext (objidlbase.h)
author: windows-sdk-content
description: Supports setting COM+ context properties.
old-location: com\icontext.htm
tech.root: com
ms.assetid: 89c41d9c-186c-4927-990d-92aa501f7d35
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IContext, IContext interface [COM], IContext interface [COM],described, _com_icontext, com.icontext, objidlbase/IContext
ms.topic: interface
req.header: objidlbase.h
req.include-header: ObjIdl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContext interface


## -description


Supports setting COM+ context properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContext</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cae291e-dcf3-43b1-8306-9e5c7a5d3be0">EnumContextProps</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a> interface pointer that can be used to enumerate the context properties in this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c6f790-9103-4cee-8a67-0f69b00ba0a1">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified context property from the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb5b282a-d337-4371-b1c2-1b429a5bf135">RemoveProperty</a>
</td>
<td align="left" width="63%">
Removes the specified context property from the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e6dc055-bc97-41e0-973c-b061e851daf5">SetProperty</a>
</td>
<td align="left" width="63%">
Adds the specified context property to the object context.

</td>
</tr>
</table> 


## -remarks



 An instance of this interface for the current context can be obtained using <a href="https://msdn.microsoft.com/97a0c6c3-a011-44dc-b428-aabdad7d4364">CoGetObjectContext</a>.



