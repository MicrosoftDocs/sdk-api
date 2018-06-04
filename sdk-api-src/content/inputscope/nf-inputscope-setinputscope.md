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

# SetInputScope function


## -description


Sets an input scope for the specified window.


## -parameters




### -param hwnd [in]

The window to set the scope on.


### -param inputscope [in]

The input scope to associate with the window. To remove the input scope association, pass IS_DEFAULT to this parameter.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method was successful.</td>
</tr>
</table>
 




## -remarks



Calling this method replaces whatever scope is associated with the window.

An application must call this method, passing in IS_DEFAULT to the <i>hwnd</i> parameter, to remove the input scope association before the window is destroyed.

This API works only when the window (<i>hwnd</i> parameter) and the calling thread are in the same thread. If you call this API for a different thread's window, it fails with E_INVALIDARG.

If you call this method on a window (<i>hwnd</i> parameter) that has 
not been associated with a Document Manager, then no text service notifications are sent to interested clients (such as the touch keyboard) that may want to respond to the 
scope change.


#### Examples

[C++]

The following code illustrates how to set an input scope for a window.

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SetInputScope(hwnd, IS_EMAIL_USERNAME);
</pre>
</td>
</tr>
</table></span></div>


