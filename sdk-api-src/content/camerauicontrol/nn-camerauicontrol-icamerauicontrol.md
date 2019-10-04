---
UID: NN:camerauicontrol.ICameraUIControl
title: ICameraUIControl (camerauicontrol.h)
author: windows-sdk-content
description: Enables a user interface control for a camera device..
old-location: winprog\icamerauicontrol.htm
tech.root: DevNotes
ms.assetid: e0fbcf43-cd52-4b5b-af4b-f7d673f7a7c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraUIControl, ICameraUIControl interface [Windows API], ICameraUIControl interface [Windows API],described, camerauicontrol/ICameraUIControl, winprog.icamerauicontrol
ms.topic: interface
f1_keywords: 
 - "camerauicontrol/ICameraUIControl"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraUIControl interface


## -description


Enables a user interface control for a camera device..


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraUIControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICameraUIControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-close">Close</a>
</td>
<td align="left" width="63%">
Closes the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-getactiveitem">GetActiveItem</a>
</td>
<td align="left" width="63%">
Gets the active captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-getcurrentviewtype">GetCurrentViewType</a>
</td>
<td align="left" width="63%">
Gets the type of the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-getselecteditems">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets the selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-removecaptureditem">RemoveCapturedItem</a>
</td>
<td align="left" width="63%">
Removes  the captured item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-resume">Resume</a>
</td>
<td align="left" width="63%">
Simulates resume of the user interface control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-show">Show</a>
</td>
<td align="left" width="63%">
Displays the user interface control for the camera.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/camerauicontrol/nf-camerauicontrol-icamerauicontrol-suspend">Suspend</a>
</td>
<td align="left" width="63%">
Simulates suspend of the user interface control.

</td>
</tr>
</table> 

