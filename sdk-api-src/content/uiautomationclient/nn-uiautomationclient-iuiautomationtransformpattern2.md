---
UID: NN:uiautomationclient.IUIAutomationTransformPattern2
title: IUIAutomationTransformPattern2 (uiautomationclient.h)
description: Extends the IUIAutomationTransformPattern interface to enable Microsoft UI Automation clients to programmatically access the viewport zooming functionality of a control.
helpviewer_keywords: ["IUIAutomationTransformPattern2","IUIAutomationTransformPattern2 interface [Windows Accessibility]","IUIAutomationTransformPattern2 interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationTransformPattern2","winauto.uiauto_IUIAutomationTransformPattern2"]
old-location: winauto\uiauto_IUIAutomationTransformPattern2.htm
tech.root: WinAuto
ms.assetid: 01585BBF-B8D7-4A69-BBB9-1B02E0864224
ms.date: 12/05/2018
ms.keywords: IUIAutomationTransformPattern2, IUIAutomationTransformPattern2 interface [Windows Accessibility], IUIAutomationTransformPattern2 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTransformPattern2, winauto.uiauto_IUIAutomationTransformPattern2
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
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTransformPattern2
 - uiautomationclient/IUIAutomationTransformPattern2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationTransformPattern2
---

# IUIAutomationTransformPattern2 interface


## -description

Extends the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a> interface to enable Microsoft UI Automation clients to programmatically access the viewport zooming functionality of a control.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTransformPattern2</b> interface inherits from <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a>. <b>IUIAutomationTransformPattern2</b> also has these types of members:
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
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-zoom">Zoom</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-zoombyunit">ZoomByUnit</a>
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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_cachedcanzoom">CachedCanZoom</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_cachedzoomlevel">CachedZoomLevel</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_cachedzoommaximum">CachedZoomMaximum</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_cachedzoomminimum">CachedZoomMinimum</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_currentcanzoom">CurrentCanZoom</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_currentzoomlevel">CurrentZoomLevel</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_currentzoommaximum">CurrentZoomMaximum</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtransformpattern2-get_currentzoomminimum">CurrentZoomMinimum</a>


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

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a>