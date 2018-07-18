---
UID: NN:camerauicontrol.ICameraUIControl
title: ICameraUIControl
author: windows-sdk-content
description: Enables a user interface control for a camera device..
old-location: winprog\icamerauicontrol.htm
old-project: devnotes
ms.assetid: e0fbcf43-cd52-4b5b-af4b-f7d673f7a7c9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICameraUIControl, ICameraUIControl interface [Windows API], ICameraUIControl interface [Windows API],described, camerauicontrol/ICameraUIControl, winprog.icamerauicontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: camerauicontrol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CameraUIControl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CALLFRAME_MARSHALCONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - camerauicontrol.h
api_name:
 - ICameraUIControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICameraUIControl interface


## -description


Enables a user interface control for a camera device..


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraUIControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICameraUIControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICameraUIControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ef05929-7292-4833-95e7-d420abb6cd43">GetActiveItem</a>
</td>
<td align="left" width="63%">
Gets the active captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1037db43-58db-4131-9a7d-d392250e133a">GetCurrentViewType</a>
</td>
<td align="left" width="63%">
Gets the type of the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/572cbf23-b9b5-441c-9bde-55ef856397ca">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets the selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/384b08e4-7683-43e1-b088-38455a0b956f">RemoveCapturedItem</a>
</td>
<td align="left" width="63%">
Removes  the captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42bd87ab-8877-48cd-abc1-6fae2cb111aa">Resume</a>
</td>
<td align="left" width="63%">
Simulates resume of the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0426a6ce-9d3e-4ce1-8be8-5d216edc9f2f">Show</a>
</td>
<td align="left" width="63%">
Displays the user interface control for the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927278">Suspend</a>
</td>
<td align="left" width="63%">
Simulates suspend of the user interface control.

</td>
</tr>
</table> 

