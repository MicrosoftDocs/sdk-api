---
UID: NN:uiautomationcore.ITransformProvider
title: ITransformProvider (uiautomationcore.h)
author: windows-sdk-content
description: Provides access to controls that can be moved, resized, and/or rotated within a two-dimensional space.
old-location: winauto\uiauto_ITransformProvider.htm
tech.root: WinAuto
ms.assetid: cdc2f81b-cf69-469f-9139-e9a73cf8c730
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransformProvider, ITransformProvider interface [Windows Accessibility], ITransformProvider interface [Windows Accessibility],described, uiauto.uiauto_ITransformProvider, uiauto_ITransformProvider, uiautomationcore/ITransformProvider, winauto.uiauto_ITransformProvider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/ITransformProvider"
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
 - ITransformProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransformProvider interface


## -description


Provides access 
        to controls that can be moved, resized, and/or rotated within a two-dimensional space.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransformProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITransformProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-move">Move</a>
</td>
<td align="left" width="63%">
Moves the control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-resize">Resize</a>
</td>
<td align="left" width="63%">
Resizes the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-rotate">Rotate</a>
</td>
<td align="left" width="63%">
Rotates the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-get_canmove">CanMove</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control can be moved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-get_canresize">CanResize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control can be resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider-get_canrotate">CanRotate</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the control can be rotated.

</td>
</tr>
</table> 


## -remarks



Implemented on a Microsoft UI Automation provider that must support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingtransform">Transform</a> control pattern.
            

Support for this  control pattern is not limited to objects on the desktop. 
            This  control pattern must also be implemented by the children of a 
            container object as long as the children can be moved, resized, or rotated freely within the boundaries of the container.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2">ITransformProvider2</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

