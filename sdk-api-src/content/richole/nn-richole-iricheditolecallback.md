---
UID: NN:richole.IRichEditOleCallback
title: IRichEditOleCallback
author: windows-sdk-content
description: The IRichEditOleCallback interface is used by a rich text edit control to retrieve OLE-related information from its client.
old-location: controls\IRichEditOleCallback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditolecallback.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRichEditOleCallback, IRichEditOleCallback interface [Windows Controls], IRichEditOleCallback interface [Windows Controls],described, _win32_IRichEditOleCallback, _win32_IRichEditOleCallback_cpp, controls.IRichEditOleCallback, controls._win32_IRichEditOleCallback, richole/IRichEditOleCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOleCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOleCallback interface


## -description


The <b>IRichEditOleCallback</b> interface is used by a rich text edit control to retrieve OLE-related information from its client. A rich edit control client is responsible for implementing this interface and assigning it to the control by using the <a href="https://msdn.microsoft.com/bd1f8048-214c-4ac6-b826-bedabb1aaee5">EM_SETOLECALLBACK</a> message.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRichEditOleCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRichEditOleCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRichEditOleCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3c7914c-6031-4193-8a7a-cb99f72c4773">ContextSensitiveHelp</a>
</td>
<td align="left" width="63%">
Indicates if the application should transition into or out of context-sensitive help mode. This method should implement the functionality described for <a href="https://msdn.microsoft.com/253f26c6-b5dd-4837-9135-96e11b4688c8">IOleWindow::ContextSensitiveHelp</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d3bc99f-e308-4cf1-acfa-51ad5bb38c4f">DeleteObject</a>
</td>
<td align="left" width="63%">
Sends notification that an object is about to be deleted from a rich edit control. The object is not necessarily being released when this member is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533eb257-3b47-405d-af4b-f4133eccffbe">GetClipboardData</a>
</td>
<td align="left" width="63%">
Allows the client to supply its own clipboard object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/760e0c36-f125-470d-b2eb-c72ed27611e1">GetContextMenu</a>
</td>
<td align="left" width="63%">
Queries the application for a context menu to use on a right-click event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77a022a0-2c3b-4d56-9506-bc26bdc74bc8">GetDragDropEffect</a>
</td>
<td align="left" width="63%">
Allows the client to specify the effects of a drop operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b0a2b6f-6d56-46ae-a071-0ce584f4a3ec">GetInPlaceContext</a>
</td>
<td align="left" width="63%">
Provides the application and document-level interfaces and information required to support in-place activation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c22dbd3-cc16-4219-965e-6ea15e07297f">GetNewStorage</a>
</td>
<td align="left" width="63%">
Provides storage for a new object pasted from the clipboard or read in from an RTF stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7daf8ea6-ffca-4a93-bf5c-4e466f3bb772">QueryAcceptData</a>
</td>
<td align="left" width="63%">
During a paste operation or a drag event, determines if the data that is pasted or dragged should be accepted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6c637e0-bd63-4870-b2fd-0fe1c7d7b897">QueryInsertObject</a>
</td>
<td align="left" width="63%">
Queries the application as to whether an object should be inserted. The member is called when pasting and when reading RTF.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eb62987-5a16-4949-aef4-2a33fd3d45e1">ShowContainerUI</a>
</td>
<td align="left" width="63%">
Indicates whether or not the application is to display its container UI. The rich edit control looks ahead for double-clicks and defers the call if appropriate. Applications may defer hiding adornments until an <a href="https://msdn.microsoft.com/7c806a02-db6d-444e-a049-22c4ae2b19b0">IOleInPlaceUIWindow::SetBorderSpace</a> call is received.

</td>
</tr>
</table> 

