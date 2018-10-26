---
UID: NN:shobjidl.INameSpaceTreeControlCustomDraw
title: INameSpaceTreeControlCustomDraw
author: windows-sdk-content
description: Exposes methods that enable the user to draw a custom namespace tree control and its items.
old-location: shell\INameSpaceTreeControlCustomDraw.htm
tech.root: shell
ms.assetid: eac7c7c2-87f0-4af1-bf2f-f4fef5ddd92e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: INameSpaceTreeControlCustomDraw, INameSpaceTreeControlCustomDraw interface [Windows Shell], INameSpaceTreeControlCustomDraw interface [Windows Shell],described, _shell_INameSpaceTreeControlCustomDraw, shell.INameSpaceTreeControlCustomDraw, shobjidl/INameSpaceTreeControlCustomDraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
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
 - Shobjidl.h
api_name:
 - INameSpaceTreeControlCustomDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControlCustomDraw interface


## -description


Exposes methods that enable the user to draw a custom namespace tree control and its items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INameSpaceTreeControlCustomDraw</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INameSpaceTreeControlCustomDraw</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INameSpaceTreeControlCustomDraw</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9da2af87-a961-4ca8-a512-fe508f2b2d79">ItemPostPaint</a>
</td>
<td align="left" width="63%">
Called after an item in the namespace tree control is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0245ecfd-2617-481a-9d34-8fc4eb0ea012">ItemPrePaint</a>
</td>
<td align="left" width="63%">
Called before an item in the namespace tree control is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe8cedc8-166d-4802-9d01-7c3991181618">PostPaint</a>
</td>
<td align="left" width="63%">
Called after the namespace tree control is drawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d9c0616-90f2-435c-a663-9ffe4adab8a0">PrePaint</a>
</td>
<td align="left" width="63%">
Called before the namespace tree control is drawn.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a>
 

 

