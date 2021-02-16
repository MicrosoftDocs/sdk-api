---
UID: NF:oleidl.IOleWindow.GetWindow
title: IOleWindow::GetWindow (oleidl.h)
description: Retrieves a handle to one of the windows participating in in-place activation (frame, document, parent, or in-place object window).
helpviewer_keywords: ["GetWindow","GetWindow method [COM]","GetWindow method [COM]","IOleWindow interface","IOleWindow interface [COM]","GetWindow method","IOleWindow.GetWindow","IOleWindow::GetWindow","_ole_iolewindow_getwindow","com.iolewindow_getwindow","oleidl/IOleWindow::GetWindow"]
old-location: com\iolewindow_getwindow.htm
tech.root: com
ms.assetid: 833adc81-be58-44a1-88f1-9aa28808e67b
ms.date: 12/05/2018
ms.keywords: GetWindow, GetWindow method [COM], GetWindow method [COM],IOleWindow interface, IOleWindow interface [COM],GetWindow method, IOleWindow.GetWindow, IOleWindow::GetWindow, _ole_iolewindow_getwindow, com.iolewindow_getwindow, oleidl/IOleWindow::GetWindow
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
 - IOleWindow::GetWindow
 - oleidl/IOleWindow::GetWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleWindow.GetWindow
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

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolewindow">IOleWindow</a>