---
UID: NN:uiautomationcore.IWindowProvider
title: IWindowProvider (uiautomationcore.h)
description: Provides access to the fundamental window-based functionality of a control.
old-location: winauto\uiauto_IWindowProvider.htm
tech.root: WinAuto
ms.assetid: cf09ad4e-fd5b-4304-b5fb-165205bff1f3
ms.date: 12/05/2018
ms.keywords: IWindowProvider, IWindowProvider interface [Windows Accessibility], IWindowProvider interface [Windows Accessibility],described, uiauto.uiauto_IWindowProvider, uiauto_IWindowProvider, uiautomationcore/IWindowProvider, winauto.uiauto_IWindowProvider
ms.topic: interface
f1_keywords:
- uiautomationcore/IWindowProvider
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IWindowProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowProvider interface


## -description


Provides 
        access to the fundamental window-based functionality of a control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWindowProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWindowProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-close">Close</a>
</td>
<td align="left" width="63%">
Attempts to close the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-setvisualstate">SetVisualState</a>
</td>
<td align="left" width="63%">
Changes the visual state of the window. For example, minimizes or maximizes it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-waitforinputidle">WaitForInputIdle</a>
</td>
<td align="left" width="63%">
Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first. 
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_canmaximize">CanMaximize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window can be maximized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_canminimize">CanMinimize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window can be minimized. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_ismodal">IsModal</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window is modal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_istopmost">IsTopmost</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the window is the topmost element in the z-order.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate">WindowInteractionState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the current state of the window for the purposes of user interaction. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate">WindowVisualState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the visual state of the window; that is, whether the window is normal (restored), minimized, or maximized.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingwindow">Window</a> control pattern.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

