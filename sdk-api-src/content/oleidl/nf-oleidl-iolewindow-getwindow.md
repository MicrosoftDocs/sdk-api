---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOleWindow::GetWindow


## -description


Retrieves a handle to one of the windows participating in in-place activation (frame, document, parent, or in-place object window).


## -parameters




### -param phwnd [out]

A pointer to a variable that receives the window handle.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The object is windowless.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>fEnterMode</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



Five types of windows comprise the windows hierarchy. When a object is active in place, it has access to some or all of these windows.

<table>
<tr>
<th>Window</th>
<th>Description</th>
</tr>
<tr>
<td>
Frame

</td>
<td>
The outermost main window where the container application's main menu resides.

</td>
</tr>
<tr>
<td>
Document

</td>
<td>
The window that displays the compound document containing the embedded object to the user.

</td>
</tr>
<tr>
<td>
Pane

</td>
<td>
The subwindow of the document window that contains the object's view. Applicable only for applications with split-pane windows.

</td>
</tr>
<tr>
<td>
Parent

</td>
<td>
The container window that contains that object's view. The object application installs its window as a child of this window.

</td>
</tr>
<tr>
<td>
In-place

</td>
<td>
The window containing the active in-place object. The object application creates this window and installs it as a child of its hatch window, which is a child of the container's parent window.

</td>
</tr>
</table>
 

Each type of window has a different role in the in-place activation architecture. However, it is not necessary to employ a separate physical window for each type. Many container applications use the same window for their frame, document, pane, and parent windows.




## -see-also




<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>
 

 

