---
UID: NN:micaut.IMathInputControl
title: IMathInputControl
author: windows-sdk-content
description: Exposes methods that turn ink input into interpreted math output.
old-location: tablet\imathinputcontrol.htm
old-project: tablet
ms.assetid: 3d6a6289-7be5-4cf0-8cb7-9095c4ee7149
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IMathInputControl, IMathInputControl interface [Tablet PC], IMathInputControl interface [Tablet PC],described, micaut/IMathInputControl, tablet.imathinputcontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: micaut.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - micaut.h
api_name:
 - IMathInputControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMathInputControl interface


## -description


The <b>IMathInputControl</b> interface exposes methods that turn ink input into interpreted math output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMathInputControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMathInputControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMathInputControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb1c9172-b520-4f6e-ae15-52634aa30007">AddFunctionName</a>
</td>
<td align="left" width="63%">
Adds a new function-name definition to the list of custom math functions that the recognizer accepts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9482f82-a08a-498d-bad0-3a1438231b23">Clear</a>
</td>
<td align="left" width="63%">
Clears all ink from the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23eae5ee-8f3d-4f54-9c30-b29f0c14ba7f">EnableAutoGrow</a>
</td>
<td align="left" width="63%">
Determines whether the control automatically grows when input is entered beyond the control's current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8cdae54-ff0b-4361-bd38-1b99137736ab">EnableExtendedButtons</a>
</td>
<td align="left" width="63%">
Determines whether the extended set of control buttons is shown.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/281695e6-295b-42d8-a184-c5a005de10e3">GetHoverIcon</a>
</td>
<td align="left" width="63%">
Retrieves the hover target icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4928f92d-7150-434c-abe4-d65a48ce1a56">GetPosition</a>
</td>
<td align="left" width="63%">
Retrieves the position and size of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b3404f5-b775-483f-b3a9-9467c937226b">GetPreviewHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height in pixels of the preview area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13b227bf-3ea5-4da1-998e-8809616d88b6">Hide</a>
</td>
<td align="left" width="63%">
Hides the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4efc0fd5-5f07-4664-8143-46a5695c04df">IsVisible</a>
</td>
<td align="left" width="63%">
Determines whether the control is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3313cb16-3400-48d5-8ba0-b3bd593b37ea">LoadInk</a>
</td>
<td align="left" width="63%">
Processes ink and triggers recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c1a16c7-4490-480d-9831-ca297ccdde80">RemoveFunctionName</a>
</td>
<td align="left" width="63%">
Removes a function-name definition from the list of custom math functions that the recognizer accepts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8790fb9b-38df-42a4-9125-2c04d46aef0b">SetCaptionText</a>
</td>
<td align="left" width="63%">
Modifies the string that will be used as the control's caption when the window is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f734b73c-88a9-45d0-a657-ff048d1f5ffe">SetCustomPaint</a>
</td>
<td align="left" width="63%">
Determines whether a button or background has custom painting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f92f731-3297-4da3-a2b9-18e1583c8b1d">SetOwnerWindow</a>
</td>
<td align="left" width="63%">
Modifies the window that owns this control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b5fc988-7c93-47d4-8661-4cef56cab0d0">SetPosition</a>
</td>
<td align="left" width="63%">
Modifies the location and size of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5e011f6-cd51-4016-ba15-c47c152bfa99">SetPreviewHeight</a>
</td>
<td align="left" width="63%">
Modifies the preview-area height in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d45d1e73-eace-4611-a4a4-28706a19766c">Show</a>
</td>
<td align="left" width="63%">
Shows the control.

</td>
</tr>
</table> 

