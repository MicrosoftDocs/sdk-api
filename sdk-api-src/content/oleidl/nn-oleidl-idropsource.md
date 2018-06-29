---
UID: NN:oleidl.IDropSource
title: IDropSource
author: windows-sdk-content
description: The IDropSource interface is one of the interfaces you implement to provide drag-and-drop operations in your application.
old-location: com\idropsource.htm
old-project: com
ms.assetid: 963a36bc-4ad7-4591-bffc-a96b4310177d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: IDropSource, IDropSource interface [COM], IDropSource interface [COM],described, _ole_idropsource, com.idropsource, oleidl/IDropSource
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IDropSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Adhocreportingexcelclient.dll
req.irql: 
req.product: ADAM
---

# IDropSource interface


## -description


The <b>IDropSource</b> interface is one of the interfaces you implement to provide drag-and-drop operations in your application. It contains methods used in any application used as a data source in a drag-and-drop operation. The data source application in a drag-and-drop operation is responsible for:
<ul>
<li>Determining the data being dragged based on the user's selection.</li>
<li>Initiating the drag-and-drop operation based on the user's mouse actions.</li>
<li>Generating some of the visual feedback during the drag-and-drop operation, such as setting the cursor and highlighting the data selected for the drag-and-drop operation.</li>
<li>Canceling or completing the drag-and-drop operation based on the user's mouse actions.</li>
<li>Performing any action on the original data caused by the drop operation, such as deleting the data on a drag move.</li>
</ul><b>IDropSource</b> contains the methods for generating visual feedback to the end user and for canceling or completing the drag-and-drop operation. You also need to call the <a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>, <a href="https://msdn.microsoft.com/00726271-4436-41f5-b7cc-666cd77216bc">RegisterDragDrop</a>, and <a href="https://msdn.microsoft.com/c0fa963c-ed06-426c-8ffc-31b02f083a23">RevokeDragDrop</a> functions in drag-and-drop operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDropSource</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IDropSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDropSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dde37299-ad7c-4f59-af99-e75b72ad9188">GiveFeedback</a>
</td>
<td align="left" width="63%">
Gives visual feedback to an end user during a drag-and-drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96ea44fc-5046-4e31-abfc-659d8ef3ca8f">QueryContinueDrag</a>
</td>
<td align="left" width="63%">
Determines whether a drag-and-drop operation should continue.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/095172ac-9e08-4797-b9da-41a4e5a61315">DoDragDrop</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/62ef4fe6-3871-41ef-9542-6fe9f3bed21c">IDropSourceNotify</a>



<a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a>
 

 

