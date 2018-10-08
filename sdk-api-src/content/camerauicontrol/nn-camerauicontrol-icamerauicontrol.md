---
UID: NN:camerauicontrol.ICameraUIControl
title: ICameraUIControl
author: windows-sdk-content
description: Enables a user interface control for a camera device..
old-location: winprog\icamerauicontrol.htm
tech.root: devnotes
ms.assetid: e0fbcf43-cd52-4b5b-af4b-f7d673f7a7c9
ms.author: windowssdkdev
ms.date: 10/05/2018
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# ICameraUIControl interface


## -description


Enables a user interface control for a camera device..


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraUIControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICameraUIControl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Hh802724(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802725(v=VS.85).aspx">GetActiveItem</a>
</td>
<td align="left" width="63%">
Gets the active captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802726(v=VS.85).aspx">GetCurrentViewType</a>
</td>
<td align="left" width="63%">
Gets the type of the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802727(v=VS.85).aspx">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets the selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802728(v=VS.85).aspx">RemoveCapturedItem</a>
</td>
<td align="left" width="63%">
Removes  the captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802729(v=VS.85).aspx">Resume</a>
</td>
<td align="left" width="63%">
Simulates resume of the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802730(v=VS.85).aspx">Show</a>
</td>
<td align="left" width="63%">
Displays the user interface control for the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Hh802731(v=VS.85).aspx">Suspend</a>
</td>
<td align="left" width="63%">
Simulates suspend of the user interface control.

</td>
</tr>
</table> 

