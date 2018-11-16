---
UID: NN:uiautomationcore.ITransformProvider2
title: ITransformProvider2
author: windows-sdk-content
description: Extends the ITransformProvider interface to enable Microsoft UI Automation providers to expose properties to support the viewport zooming functionality of a control.
old-location: winauto\uiauto_ITransformProvider2.htm
tech.root: WinAuto
ms.assetid: 763F30BC-782A-43ED-9DE4-97A237D7B9F8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITransformProvider2, ITransformProvider2 interface [Windows Accessibility], ITransformProvider2 interface [Windows Accessibility],described, uiautomationcore/ITransformProvider2, winauto.uiauto_ITransformProvider2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransformProvider2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a> interface to enable Microsoft UI Automation providers to expose properties to support the viewport zooming functionality of a control.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransformProvider2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B267DAB1-F78B-4543-9A90-7107E5259A0C">Zoom</a>
</td>
<td align="left" width="63%">
Zooms the viewport of the control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FB75D568-A1E4-4B39-A0FE-FE42E79C93B2">ZoomByUnit</a>
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

<a href="https://msdn.microsoft.com/D7B323C1-D33C-4685-99A0-A5F3E8F3A605">CanZoom</a>


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

<a href="https://msdn.microsoft.com/AFC38A55-C2E4-4E5A-AD52-AE0CE96F86AC">ZoomLevel</a>


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

<a href="https://msdn.microsoft.com/92C36184-ACFB-4120-B0E6-A0E615855567">ZoomMaximum</a>


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

<a href="https://msdn.microsoft.com/823C5043-214F-455E-8F6F-172A097A169F">ZoomMinimum</a>


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




<a href="https://msdn.microsoft.com/08d0226d-845c-4564-a059-539b62fc7909">Control Pattern Interfaces for Providers</a>



<a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a>
 

 

