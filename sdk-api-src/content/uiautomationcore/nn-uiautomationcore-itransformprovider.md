---
UID: NN:uiautomationcore.ITransformProvider
title: ITransformProvider
author: windows-sdk-content
description: Provides access to controls that can be moved, resized, and/or rotated within a two-dimensional space.
old-location: winauto\uiauto_ITransformProvider.htm
old-project: WinAuto
ms.assetid: cdc2f81b-cf69-469f-9139-e9a73cf8c730
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ITransformProvider, ITransformProvider interface [Windows Accessibility], ITransformProvider interface [Windows Accessibility],described, uiauto.uiauto_ITransformProvider, uiauto_ITransformProvider, uiautomationcore/ITransformProvider, winauto.uiauto_ITransformProvider
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
 - ITransformProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITransformProvider interface


## -description



        Provides access 
        to controls that can be moved, resized, and/or rotated within a two-dimensional space.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITransformProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITransformProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5abd6b54-a555-4e6f-9868-9c9b3e2f6e50">Move</a>
</td>
<td align="left" width="63%">
Moves the control. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba22f770-1306-4c15-bc72-a928b91e0eb5">Resize</a>
</td>
<td align="left" width="63%">
Resizes the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e8255de-b28d-4fc4-82ea-4255771f9838">Rotate</a>
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

<a href="https://msdn.microsoft.com/82392d66-2a9d-4951-a687-833737d424ec">CanMove</a>


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

<a href="https://msdn.microsoft.com/fd7cb359-6e71-44c2-b1c0-4fd7e210244e">CanResize</a>


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

<a href="https://msdn.microsoft.com/9943a5d7-916d-4546-8aba-fe5abe3e4eb2">CanRotate</a>


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




            Implemented on a Microsoft UI Automation provider that must support the <a href="https://msdn.microsoft.com/e1d862a0-8085-42b4-9710-cf11e1a467cf">Transform</a> control pattern.
            


            Support for this  control pattern is not limited to objects on the desktop. 
            This  control pattern must also be implemented by the children of a 
            container object as long as the children can be moved, resized, or rotated freely within the boundaries of the container.
            




## -see-also




<a href="https://msdn.microsoft.com/763F30BC-782A-43ED-9DE4-97A237D7B9F8">ITransformProvider2</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

