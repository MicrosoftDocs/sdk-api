---
UID: NN:shlobj.IDockingWindowFrame
title: IDockingWindowFrame
author: windows-sdk-content
description: Exposes methods that support the addition of IDockingWindow objects to a frame. Implemented by the browser.
old-location: shell\IDockingWindowFrame.htm
tech.root: shell
ms.assetid: d0dc10db-316a-4eaa-83db-3f186ee77071
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IDockingWindowFrame, IDockingWindowFrame interface [Windows Shell], IDockingWindowFrame interface [Windows Shell],described, _win32_IDockingWindowFrame, shell.IDockingWindowFrame, shlobj/IDockingWindowFrame
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDockingWindowFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindowFrame interface


## -description


Exposes methods that support the addition of <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> objects to a frame. Implemented by the browser.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockingWindowFrame</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IDockingWindowFrame</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDockingWindowFrame</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b046bb62-8bc1-4021-bcb2-d4f23a9fccf4">AddToolbar</a>
</td>
<td align="left" width="63%">
Adds the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object to the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9086f8ae-6a81-463d-9482-7a60701ab8de">FindToolbar</a>
</td>
<td align="left" width="63%">
Finds the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object in the toolbar frame and returns an interface pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ebc4561-a7fe-4fa4-ae2a-88030ede02e7">RemoveToolbar</a>
</td>
<td align="left" width="63%">
Removes the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> from the toolbar frame.

</td>
</tr>
</table> 


## -remarks



<b>IDockingWindowFrame</b> is derived from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindowFrame</b> through that inheritance.

<table class="clsStd">
<tr>
<th>Additional IDockingWindowFrame Methods</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IOleWindow::GetWindow</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/253f26c6-b5dd-4837-9135-96e11b4688c8">IOleWindow::ContextSensitiveHelp</a>
</td>
</tr>
</table>
 

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
You do not typically implement the <b>IDockingWindowFrame</b> interface. The Shell browser implements this interface to support docked windows inside the browser frame.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You use <b>IDockingWindowFrame</b> to add, find, and remove docking window objects in a browser frame.



