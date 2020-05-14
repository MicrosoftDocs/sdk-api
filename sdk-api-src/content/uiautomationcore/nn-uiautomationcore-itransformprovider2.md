---
UID: NN:uiautomationcore.ITransformProvider2
title: ITransformProvider2 (uiautomationcore.h)
description: Extends the ITransformProvider interface to enable Microsoft UI Automation providers to expose properties to support the viewport zooming functionality of a control.helpviewer_keywords: ["ITransformProvider2","ITransformProvider2 interface [Windows Accessibility]","ITransformProvider2 interface [Windows Accessibility]","described","uiautomationcore/ITransformProvider2","winauto.uiauto_ITransformProvider2"]
old-location: winauto\uiauto_ITransformProvider2.htm
tech.root: WinAuto
ms.assetid: 763F30BC-782A-43ED-9DE4-97A237D7B9F8
ms.date: 12/05/2018
ms.keywords: ITransformProvider2, ITransformProvider2 interface [Windows Accessibility], ITransformProvider2 interface [Windows Accessibility],described, uiautomationcore/ITransformProvider2, winauto.uiauto_ITransformProvider2
f1_keywords:
- uiautomationcore/ITransformProvider2
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- ITransformProvider2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransformProvider2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a> interface to enable Microsoft UI Automation providers to expose properties to support the viewport zooming functionality of a control.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransformProvider2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITransformProvider2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom">Zoom</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoombyunit">ZoomByUnit</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control by the specified logical unit.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom">CanZoom</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_zoomlevel">ZoomLevel</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the current zoom level of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_zoommaximum">ZoomMaximum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the maximum zoom level of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_zoomminimum">ZoomMinimum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minimum zoom level of the element.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-cpinterfaces">Control Pattern Interfaces for Providers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a>
 

 

