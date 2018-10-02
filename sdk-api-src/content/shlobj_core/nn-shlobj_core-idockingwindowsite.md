---
UID: NN:shlobj_core.IDockingWindowSite
title: IDockingWindowSite
author: windows-sdk-content
description: Exposes methods that manage the border space for one or more IDockingWindow objects. This interface is implemented by the browser and is similar to the IOleInPlaceUIWindow interface.
old-location: shell\IDockingWindowSite.htm
tech.root: Shell
ms.assetid: 7418a6af-74ce-4435-8ed9-af106df0f95b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IDockingWindowSite, IDockingWindowSite interface [Windows Shell], IDockingWindowSite interface [Windows Shell],described, _win32_IDockingWindowSite, shell.IDockingWindowSite, shlobj_core/IDockingWindowSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
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
 - IDockingWindowSite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockingWindowSite interface


## -description


Exposes methods that manage the border space for one or more <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> objects. This interface is implemented by the browser and is similar to the <a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDockingWindowSite</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IDockingWindowSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDockingWindowSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1c30a49-8d87-4855-acc0-5f33eabe5e8a">GetBorderDW</a>
</td>
<td align="left" width="63%">
Gets the border space allocated for the specified <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a104c58b-44da-47e7-b10b-f0116024bee1">RequestBorderSpaceDW</a>
</td>
<td align="left" width="63%">
Approves, modifies, or refuses a request for an <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object's border space. The border space is not allocated until the <a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a> method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c79c983-8a5d-4b52-848d-c85c4e4f86ec">SetBorderSpaceDW</a>
</td>
<td align="left" width="63%">
Allocates and reserves border space for an <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> object.

</td>
</tr>
</table> 


## -remarks



<b>IDockingWindowSite</b> is derived from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. See the following topics for details on these methods also available to <b>IDockingWindowSite</b> through that inheritance.



<table class="clsStd">
<tr>
<th>Additional IDockingWindowSite Methods</th>
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
You do not typically implement the <b>IDockingWindowSite</b> interface. The Shell browser implements this interface to support docked windows inside the browser frame.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
You use <b>IDockingWindowSite</b> to negotiate the space for a docking window object in a browser frame.



