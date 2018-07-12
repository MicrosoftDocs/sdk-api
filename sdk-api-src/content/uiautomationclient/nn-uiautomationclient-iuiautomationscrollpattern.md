---
UID: NN:uiautomationclient.IUIAutomationScrollPattern
title: IUIAutomationScrollPattern
author: windows-sdk-content
description: Provides access to a control that acts as a scrollable container for a collection of child elements.
old-location: winauto\uiauto_IUIAutomationScrollPattern.htm
old-project: WinAuto
ms.assetid: cb62389c-5a7a-412d-a024-0ce9bc6403a2
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IUIAutomationScrollPattern, IUIAutomationScrollPattern interface [Windows Accessibility], IUIAutomationScrollPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationScrollPattern, uiauto_IUIAutomationScrollPattern, uiautomationclient/IUIAutomationScrollPattern, winauto.uiauto_IUIAutomationScrollPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationScrollPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationScrollPattern interface


## -description


Provides access to a  control that acts as a scrollable container for a collection of child elements. The children of this element support <a href="https://msdn.microsoft.com/16f0ec7d-6c96-479f-8b8d-397f76d681aa">IUIAutomationScrollItemPattern</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationScrollPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationScrollPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationScrollPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2deb7399-604d-45eb-95d6-f1135550a18f">Scroll</a>
</td>
<td align="left" width="63%">
Scrolls the visible region of the content area horizontally and vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f31445d-6198-430a-8f31-3ff25b72581c">SetScrollPercent</a>
</td>
<td align="left" width="63%">
Sets the horizontal and vertical scroll positions as a percentage of the total content area within the UI Automation element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationScrollPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9089e237-2115-47b6-a1eb-eaea5a93586e">CachedHorizontallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element can scroll horizontally.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8cdc76fc-dfac-462e-977f-e216fce43607">CachedHorizontalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached horizontal scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/948f29d5-6e3b-4eb7-b0de-cf78e7ea956a">CachedHorizontalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached horizontal size of the viewable region of a scrollable element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e9e55853-6fe3-4e51-bb4c-aea0174ed710">CachedVerticallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element can scroll vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e2b7fb86-1a2b-4b49-8c8f-73445327e4d6">CachedVerticalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached vertical scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d0fedff8-27b7-403c-a431-345605045458">CachedVerticalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached vertical size of the viewable region of a scrollable element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4107440a-4bfc-42df-87b0-47b9eb3ce2e6">CurrentHorizontallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element can scroll horizontally.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dd882f92-be09-49c8-b2fc-fe54f661c686">CurrentHorizontalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the horizontal scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/523b4c3e-f48e-4486-981b-8996a4d36ae3">CurrentHorizontalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the horizontal size of the viewable region of a scrollable element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/decadcaa-da60-4c87-ab9c-92fc4e233fa1">CurrentVerticallyScrollable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element can scroll vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/45b45faa-a147-4c05-82ca-878d46c71af0">CurrentVerticalScrollPercent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the vertical scroll position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a87f617-fd98-497b-b7fd-8b2c901fe1eb">CurrentVerticalViewSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the vertical size of the viewable region of a scrollable element.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

