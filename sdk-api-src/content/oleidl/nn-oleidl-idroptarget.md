---
UID: NN:oleidl.IDropTarget
title: IDropTarget
author: windows-sdk-content
description: The IDropTarget interface is one of the interfaces you implement to provide drag-and-drop operations in your application.
old-location: com\idroptarget.htm
tech.root: com
ms.assetid: 13fbe834-1ef8-4944-b2e4-9f5c413c65c8
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IDropTarget, IDropTarget interface [COM], IDropTarget interface [COM],described, _ole_idroptarget, com.idroptarget, oleidl/IDropTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IDropTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDropTarget interface


## -description


The <b>IDropTarget</b> interface is one of the interfaces you implement to provide drag-and-drop operations in your application. It contains methods used in any application that can be a target for data during a drag-and-drop operation. A drop-target application is responsible for:
<ul>
<li>Determining the effect of the drop on the target application.</li>
<li>Incorporating any valid dropped data when the drop occurs.</li>
<li>Communicating target feedback to the source so the source application can provide appropriate visual feedback such as setting the cursor.</li>
<li>Implementing drag scrolling.</li>
<li>Registering and revoking its application windows as drop targets.</li>
</ul>The <b>IDropTarget</b> interface contains methods that handle all these responsibilities except registering and revoking the application window as a drop target, for which you must call the <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a> and the <a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a> functions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropTarget</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IDropTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDropTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e4d7013-910c-4a6e-8eee-818e1f2302ac">DragEnter</a>
</td>
<td align="left" width="63%">
Determines whether a drop can be accepted and its effect if it is accepted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f2f1bdb-e57c-42e2-9afb-65b13cdc22f8">DragLeave</a>
</td>
<td align="left" width="63%">
Causes the drop target to suspend its feedback actions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31bb71dd-eed7-48f9-9f6c-f5d7f9d4118e">DragOver</a>
</td>
<td align="left" width="63%">
Provides target feedback to the user through the <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a> function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ea6d815-bf8f-47d5-99d3-f9a55bafee2e">Drop</a>
</td>
<td align="left" width="63%">
Drops the data into the target window.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>



<a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>



<a href="https://msdn.microsoft.com/62ef4fe6-3871-41ef-9542-6fe9f3bed21c">IDropSourceNotify</a>



<a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>



<a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a>
 

 

