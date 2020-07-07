---
UID: NN:micaut.IMathInputControl
title: IMathInputControl (micaut.h)
description: Exposes methods that turn ink input into interpreted math output.
helpviewer_keywords: ["IMathInputControl","IMathInputControl interface [Tablet PC]","IMathInputControl interface [Tablet PC]","described","micaut/IMathInputControl","tablet.imathinputcontrol"]
old-location: tablet\imathinputcontrol.htm
tech.root: tablet
ms.assetid: 3d6a6289-7be5-4cf0-8cb7-9095c4ee7149
ms.date: 12/05/2018
ms.keywords: IMathInputControl, IMathInputControl interface [Tablet PC], IMathInputControl interface [Tablet PC],described, micaut/IMathInputControl, tablet.imathinputcontrol
f1_keywords:
- micaut/IMathInputControl
dev_langs:
- c++
req.header: micaut.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- micaut.h
api_name:
- IMathInputControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMathInputControl interface


## -description


The <b>IMathInputControl</b> interface exposes methods that turn ink input into interpreted math output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMathInputControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMathInputControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-addfunctionname">AddFunctionName</a>
</td>
<td align="left" width="63%">
Adds a new function-name definition to the list of custom math functions that the recognizer accepts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears all ink from the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-enableautogrow">EnableAutoGrow</a>
</td>
<td align="left" width="63%">
Determines whether the control automatically grows when input is entered beyond the control's current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-enableextendedbuttons">EnableExtendedButtons</a>
</td>
<td align="left" width="63%">
Determines whether the extended set of control buttons is shown.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-gethovericon">GetHoverIcon</a>
</td>
<td align="left" width="63%">
Retrieves the hover target icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Retrieves the position and size of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-getpreviewheight">GetPreviewHeight</a>
</td>
<td align="left" width="63%">
Retrieves the height in pixels of the preview area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-hide">Hide</a>
</td>
<td align="left" width="63%">
Hides the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-isvisible">IsVisible</a>
</td>
<td align="left" width="63%">
Determines whether the control is visible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-loadink">LoadInk</a>
</td>
<td align="left" width="63%">
Processes ink and triggers recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-removefunctionname">RemoveFunctionName</a>
</td>
<td align="left" width="63%">
Removes a function-name definition from the list of custom math functions that the recognizer accepts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setcaptiontext">SetCaptionText</a>
</td>
<td align="left" width="63%">
Modifies the string that will be used as the control's caption when the window is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setcustompaint">SetCustomPaint</a>
</td>
<td align="left" width="63%">
Determines whether a button or background has custom painting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setownerwindow">SetOwnerWindow</a>
</td>
<td align="left" width="63%">
Modifies the window that owns this control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setposition">SetPosition</a>
</td>
<td align="left" width="63%">
Modifies the location and size of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-setpreviewheight">SetPreviewHeight</a>
</td>
<td align="left" width="63%">
Modifies the preview-area height in pixels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show">Show</a>
</td>
<td align="left" width="63%">
Shows the control.

</td>
</tr>
</table> 

