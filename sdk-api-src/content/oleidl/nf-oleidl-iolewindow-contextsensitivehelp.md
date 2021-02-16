---
UID: NF:oleidl.IOleWindow.ContextSensitiveHelp
title: IOleWindow::ContextSensitiveHelp (oleidl.h)
description: Determines whether context-sensitive help mode should be entered during an in-place activation session.
helpviewer_keywords: ["ContextSensitiveHelp","ContextSensitiveHelp method [COM]","ContextSensitiveHelp method [COM]","IOleWindow interface","IOleInPlaceSiteWindowless.ContextSensitiveHelp","IOleWindow interface [COM]","ContextSensitiveHelp method","IOleWindow.ContextSensitiveHelp","IOleWindow::ContextSensitiveHelp","_ole_iolewindow_contextsensitivehelp","com.iolewindow_contextsensitivehelp","oleidl/IOleWindow::ContextSensitiveHelp"]
old-location: com\iolewindow_contextsensitivehelp.htm
tech.root: com
ms.assetid: 253f26c6-b5dd-4837-9135-96e11b4688c8
ms.date: 12/05/2018
ms.keywords: ContextSensitiveHelp, ContextSensitiveHelp method [COM], ContextSensitiveHelp method [COM],IOleWindow interface, IOleInPlaceSiteWindowless.ContextSensitiveHelp, IOleWindow interface [COM],ContextSensitiveHelp method, IOleWindow.ContextSensitiveHelp, IOleWindow::ContextSensitiveHelp, _ole_iolewindow_contextsensitivehelp, com.iolewindow_contextsensitivehelp, oleidl/IOleWindow::ContextSensitiveHelp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleWindow::ContextSensitiveHelp
 - oleidl/IOleWindow::ContextSensitiveHelp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
 - browsewm.dll
api_name:
 - IOleWindow.ContextSensitiveHelp
 - IOleInPlaceSiteWindowless.ContextSensitiveHelp
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

If a container application is to support context-sensitive help on menu items, it must either provide its own message filter so that it can intercept the F1 key or ask the OLE library to add a message filter by calling <a href="/windows/desktop/api/ole2/nf-ole2-olesetmenudescriptor">OleSetMenuDescriptor</a>, passing valid, non-<b>NULL</b> values for the <i>lpFrame</i> and <i>lpActiveObj</i> parameters.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olesetmenudescriptor">OleSetMenuDescriptor</a>