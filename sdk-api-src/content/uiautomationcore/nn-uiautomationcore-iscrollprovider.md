---
UID: NN:uiautomationcore.IScrollProvider
title: IScrollProvider (uiautomationcore.h)
author: windows-sdk-content
description: Provides access to controls that act as scrollable containers for a collection of child objects.
old-location: winauto\uiauto_IScrollProvider.htm
tech.root: WinAuto
ms.assetid: 55e1b899-aa9f-45eb-9cfa-d645ea659988
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IScrollProvider, IScrollProvider interface [Windows Accessibility], IScrollProvider interface [Windows Accessibility],described, uiauto.uiauto_IScrollProvider, uiauto_IScrollProvider, uiautomationcore/IScrollProvider, winauto.uiauto_IScrollProvider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IScrollProvider"
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
ms.custom: 19H1
---

# IScrollProvider interface


## -description


Provides access 
        to controls that act as scrollable containers for a collection of child objects. 
        The children of this control must implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollitemprovider">IScrollItemProvider</a>.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScrollProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IScrollProvider</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-scroll">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls the visible region of the content area horizontally and vertically.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-setscrollpercent">SetScrollPercent</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable">HorizontallyScrollable</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent">HorizontalScrollPercent</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize">HorizontalViewSize</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable">VerticallyScrollable</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent">VerticalScrollPercent</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize">VerticalViewSize</a>


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
            support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingscroll">Scroll</a> control pattern.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

