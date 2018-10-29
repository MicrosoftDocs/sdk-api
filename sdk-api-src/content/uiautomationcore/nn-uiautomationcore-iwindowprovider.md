---
UID: NN:uiautomationcore.IWindowProvider
title: IWindowProvider
author: windows-sdk-content
description: Provides access to the fundamental window-based functionality of a control.
old-location: winauto\uiauto_IWindowProvider.htm
tech.root: WinAuto
ms.assetid: cf09ad4e-fd5b-4304-b5fb-165205bff1f3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWindowProvider, IWindowProvider interface [Windows Accessibility], IWindowProvider interface [Windows Accessibility],described, uiauto.uiauto_IWindowProvider, uiauto_IWindowProvider, uiautomationcore/IWindowProvider, winauto.uiauto_IWindowProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowProvider interface


## -description


Provides 
        access to the fundamental window-based functionality of a control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWindowProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3bfd7801-c296-4f59-8094-c13c8f044038">Close</a>
</td>
<td align="left" width="63%">
Attempts to close the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89239900-5ee4-4f3a-a398-6ceb4846caf9">SetVisualState</a>
</td>
<td align="left" width="63%">
Changes the visual state of the window. For example, minimizes or maximizes it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/787f8309-09aa-4e6a-bfbc-fc03b917ead4">WaitForInputIdle</a>
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

<a href="https://msdn.microsoft.com/d3ff456a-c17d-4500-a141-87e9dd3fbfd0">CanMaximize</a>


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

<a href="https://msdn.microsoft.com/0dc62d89-adf7-4fb5-b77d-07c9682c11af">CanMinimize</a>


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

<a href="https://msdn.microsoft.com/16b1adb3-2816-4f7d-a805-8fc238ad78e4">IsModal</a>


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

<a href="https://msdn.microsoft.com/53181d04-112f-4e38-a2ab-760f215defc6">IsTopmost</a>


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

<a href="https://msdn.microsoft.com/b7fcd5e6-1232-4096-a913-5fd870c83e62">WindowInteractionState</a>


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

<a href="https://msdn.microsoft.com/c65e8687-51b7-45ea-8183-6d9674f77012">WindowVisualState</a>


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



Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/bfd37d27-fcec-4d25-841c-63e14e48c6c8">Window</a> control pattern.





## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

