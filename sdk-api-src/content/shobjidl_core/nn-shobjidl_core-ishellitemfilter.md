---
UID: NN:shobjidl_core.IShellItemFilter
title: IShellItemFilter
author: windows-sdk-content
description: Exposed by a client to specify how to filter the enumeration of a Shell item by a server application.
old-location: shell\IShellItemFilter.htm
tech.root: shell
ms.assetid: c2873385-a25d-4d9d-94ef-05dcdf284be1
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IShellItemFilter, IShellItemFilter interface [Windows Shell], IShellItemFilter interface [Windows Shell],described, _shell_IShellItemFilter, shell.IShellItemFilter, shobjidl_core/IShellItemFilter
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
 - IShellItemFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemFilter interface


## -description


Exposed by a client to specify how to filter the enumeration of a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> by a server application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellItemFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellItemFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellItemFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a84868ab-25c4-4cb7-84a1-aba0eff09b4a">GetEnumFlagsForItem</a>
</td>
<td align="left" width="63%">
Allows a client to specify which classes of objects in a <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> should be enumerated for inclusion in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ec171e-24a0-40ff-b199-36b5a2809164">IncludeItem</a>
</td>
<td align="left" width="63%">
Sets a given <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">Shell item</a> status to inclusion in the view.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

