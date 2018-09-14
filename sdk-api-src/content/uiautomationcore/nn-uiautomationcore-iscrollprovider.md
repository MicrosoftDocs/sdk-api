---
UID: NN:uiautomationcore.IScrollProvider
title: IScrollProvider
author: windows-sdk-content
description: Provides access to controls that act as scrollable containers for a collection of child objects.
old-location: winauto\uiauto_IScrollProvider.htm
tech.root: WinAuto
ms.assetid: 55e1b899-aa9f-45eb-9cfa-d645ea659988
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IScrollProvider, IScrollProvider interface [Windows Accessibility], IScrollProvider interface [Windows Accessibility],described, uiauto.uiauto_IScrollProvider, uiauto_IScrollProvider, uiautomationcore/IScrollProvider, winauto.uiauto_IScrollProvider
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
 - IScrollProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IScrollProvider interface


## -description


Provides access 
        to controls that act as scrollable containers for a collection of child objects. 
        The children of this control must implement <a href="https://msdn.microsoft.com/d8a8384e-d57b-4614-a643-b5ba3a63224d">IScrollItemProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScrollProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IScrollProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IScrollProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1bd15d2-beaf-4838-970a-00cfa2a7cfd9">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls the visible region of the content area horizontally and vertically.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4949fd00-6678-4278-b11b-cc8503e67de2">SetScrollPercent</a>
</td>
<td align="left" width="63%">
Sets the horizontal and vertical scroll position as a percentage of the total content area within the control.
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScrollProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f9d073c0-b51a-4e62-ab67-872538a6a0e1">HorizontallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control can scroll horizontally.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/02affb6c-cacb-4305-beb3-7ccef8f0662a">HorizontalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the horizontal scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b23c2e67-6bab-44c8-b52d-60329851d689">HorizontalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the horizontal 
                size of the viewable region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fadc0fd7-969c-4189-b37c-9b8243e30ac1">VerticallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control can scroll vertically.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1bc153bf-1d8f-4ca6-88e0-882e063fe6a0">VerticalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the vertical scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9ddf60c9-68d4-4bec-8bbe-cb9bb13711e6">VerticalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the vertical 
                size of the viewable region.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must 
            support the <a href="https://msdn.microsoft.com/baf8012a-52d5-4465-b26d-aa3d7f550b54">Scroll</a> control pattern.
            




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

