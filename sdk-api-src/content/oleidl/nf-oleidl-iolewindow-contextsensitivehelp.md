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

# IOleWindow::ContextSensitiveHelp


## -description


Determines whether context-sensitive help mode should be entered during an in-place activation session.


## -parameters




### -param fEnterMode [in]

<b>TRUE</b> if help mode should be entered; <b>FALSE</b> if it should be exited.


## -returns



This method returns S_OK if the help mode was entered or exited successfully, depending on the value passed in <i>fEnterMode</i>. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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



Applications can invoke context-sensitive help when the user:

<ul>
<li>presses SHIFT+F1, then clicks a topic</li>
<li>presses F1 when a menu item is selected</li>
</ul>
When SHIFT+F1 is pressed, either the frame or active object can receive the keystrokes. If the container's frame receives the keystrokes, it calls its containing document's <b>IOleWindow::ContextSensitiveHelp</b> method with <i>fEnterMode</i> set to <b>TRUE</b>. This propagates the help state to all of its in-place objects so they can correctly handle the mouse click or WM_COMMAND.

If an active object receives the SHIFT+F1 keystrokes, it calls the container's <b>IOleWindow::ContextSensitiveHelp</b> method with <i>fEnterMode</i><b>TRUE</b>, which then recursively calls each of its in-place sites until there are no more to be notified. The container then calls its document's or frame's <b>IOleWindow::ContextSensitiveHelp</b> method with <i>fEnterMode</i><b>TRUE</b>.

When in context-sensitive help mode, an object that receives the mouse click can either:

<ul>
<li>Ignore the click if it does not support context-sensitive help.</li>
<li>Tell all the other objects to exit context-sensitive help mode with <b>ContextSensitiveHelp</b> set to <b>FALSE</b> and then provide help for that context.</li>
</ul>
An object in context-sensitive help mode that receives a WM_COMMAND should tell all the other in-place objects to exit context-sensitive help mode and then provide help for the command.

If a container application is to support context-sensitive help on menu items, it must either provide its own message filter so that it can intercept the F1 key or ask the OLE library to add a message filter by calling <a href="https://msdn.microsoft.com/c80fe36d-5093-4814-83a9-0c11c5a7cf5f">OleSetMenuDescriptor</a>, passing valid, non-<b>NULL</b> values for the <i>lpFrame</i> and <i>lpActiveObj</i> parameters.




## -see-also




<a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>



<a href="https://msdn.microsoft.com/c80fe36d-5093-4814-83a9-0c11c5a7cf5f">OleSetMenuDescriptor</a>
 

 

