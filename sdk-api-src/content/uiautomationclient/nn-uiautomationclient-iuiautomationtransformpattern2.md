---
UID: NN:uiautomationclient.IUIAutomationTransformPattern2
title: IUIAutomationTransformPattern2
author: windows-sdk-content
description: Extends the IUIAutomationTransformPattern interface to enable Microsoft UI Automation clients to programmatically access the viewport zooming functionality of a control.
old-location: winauto\uiauto_IUIAutomationTransformPattern2.htm
old-project: WinAuto
ms.assetid: 01585BBF-B8D7-4A69-BBB9-1B02E0864224
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IUIAutomationTransformPattern2, IUIAutomationTransformPattern2 interface [Windows Accessibility], IUIAutomationTransformPattern2 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTransformPattern2, winauto.uiauto_IUIAutomationTransformPattern2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTransformPattern2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTransformPattern2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/276b44d9-a335-4d4e-8fe9-de03584dadb4">IUIAutomationTransformPattern</a> interface to enable Microsoft UI Automation clients to programmatically access the viewport zooming functionality of a control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTransformPattern2</b> interface inherits from <a href="https://msdn.microsoft.com/276b44d9-a335-4d4e-8fe9-de03584dadb4">IUIAutomationTransformPattern</a>. <b>IUIAutomationTransformPattern2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTransformPattern2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7CCDDF69-32FA-486C-B319-4D2F7A2407B4">Zoom</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F46358F0-991B-45E1-AEEF-F6EB43B50202">ZoomByUnit</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control by the specified unit.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTransformPattern2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/36C0CEFE-8035-42CF-B480-7C9BA02F7BB3">CachedCanZoom</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the control supports zooming of its viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9A0F0459-97F7-44C0-B7F8-11593A69DEBA">CachedZoomLevel</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached zoom level of the control's viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/482C482F-299D-4948-A794-79F3F7465F8D">CachedZoomMaximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached maximum zoom level of the control's viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/26C56849-204A-47B3-8734-7A16F5577357">CachedZoomMinimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached minimum zoom level of the control's viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9807080C-2E62-4B3E-AED5-7847748737E3">CurrentCanZoom</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control supports zooming of its viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/AE4A83CF-FB24-4649-BB8C-88A03B96E8D9">CurrentZoomLevel</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the zoom level of the control's viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/600A6FCC-7B67-435A-B162-BC0EC8D609B0">CurrentZoomMaximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the maximum zoom level of the control's viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9393D635-016D-4A31-BCB2-DC4100D7D1CB">CurrentZoomMinimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum zoom level of the control's viewport.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>



<a href="https://msdn.microsoft.com/276b44d9-a335-4d4e-8fe9-de03584dadb4">IUIAutomationTransformPattern</a>
 

 

