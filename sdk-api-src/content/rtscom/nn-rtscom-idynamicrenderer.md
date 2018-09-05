---
UID: NN:rtscom.IDynamicRenderer
title: IDynamicRenderer
author: windows-sdk-content
description: Displays the tablet pen data in real-time as that data is being handled by the RealTimeStylus Class object.
old-location: tablet\idynamicrenderer.htm
old-project: tablet
ms.assetid: 6435b297-d6a7-418b-afc0-f8cc0b329842
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 6435b297-d6a7-418b-afc0-f8cc0b329842, IDynamicRenderer, IDynamicRenderer interface [Tablet PC], IDynamicRenderer interface [Tablet PC],described, rtscom/IDynamicRenderer, tablet.idynamicrenderer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: rtscom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IDynamicRenderer interface


## -description



Displays the tablet pen data in real-time as that data is being handled by the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDynamicRenderer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDynamicRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDynamicRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0f05fc7-2b54-40fc-823a-dad0a86174d6">Draw</a>
</td>
<td align="left" width="63%">
Draws the cached data to the specified device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/409d4353-fc85-49ff-99a4-d8393a3c0ec4">Refresh</a>
</td>
<td align="left" width="63%">
Makes the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object refresh the data that it's currently rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">ReleaseCachedData</a>
</td>
<td align="left" width="63%">
Releases specified stroke data from the temporal data held by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDynamicRenderer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d3c6d2e-1675-4335-a283-ea14a818469a">ClipRectangle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the clipping rectangle for the dynamic renderer. Defaults to <b>NULL</b>.

Default is {0,0,0,0}. Coordinates are in pixels

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf11d03d-8f60-44aa-a296-cc44ddc3930a">ClipRegion</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the clipping region for the dynamic renderer. Defaults to <b>NULL</b>. Setting the clipping region does not trigger a redraw.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">DataCacheEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Allows the caller to specify whether to use the <a href="https://msdn.microsoft.com/691de815-a5be-4982-a59a-b904c070ede8">IDynamicRenderer::ReleaseCachedData Method</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">DrawingAttributes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a> object used by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object. Allows the caller to set or modify the drawing attributes for the next stroke. Device rendering should not be using the <b>DynamicRenderer Class</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b226d146-af96-4a51-aa11-8b2fe057a4b2">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Allows the caller to turn dynamic rendering on and off. The default is <b>false</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1795100f-d529-4513-8635-65d1d7285f72">HWND</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the <a href="https://msdn.microsoft.com/1795100f-d529-4513-8635-65d1d7285f72">IDynamicRenderer::HWND Property</a> associated with the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object. Defaults to <b>NULL</b>

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>.

The <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> renders packet data dynamically.

Be sure the set the handle of the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> before you add it to a plug-in collection on the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>. If the handle is not set, the <a href="https://msdn.microsoft.com/236589f8-a6ae-4db3-8be4-68c5babeb9f0">IStylusPlugin::Error Method</a> notification method on each plug-in is called. For more information see <a href="https://msdn.microsoft.com/7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b">Error Handling Considerations for the StylusInput APIs</a>.

The <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> implements the <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> interface.

A <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object can redraw the ink when a window has been invalidated.

While it is possible to have a given plug-in associated with multiple <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> objects, the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> and <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> plug-ins are not designed to support this.

<div class="alert"><b>Note</b>  Calling interface members directly without the intervention of a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> instance is not supported.</div>
<div> </div>
The <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> has two categories of properties: those for which changes take effect immediately and those for which changes take effect upon the next <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a> event notification. The <a href="https://msdn.microsoft.com/0d3c6d2e-1675-4335-a283-ea14a818469a">IDynamicRenderer::ClipRectangle Property</a> property takes effect immediately, enabling the text input area to grow dynamically as the user writes. The other properties take effect after the next <b>IStylusPlugin::StylusDown Method</b> event notification.

The following are the properties for which changes take immediate effect:


<a href="https://msdn.microsoft.com/0d3c6d2e-1675-4335-a283-ea14a818469a">IDynamicRenderer::ClipRectangle Property</a>


The following are the properties for which changes do not take immediate effect and are delayed:


<a href="https://msdn.microsoft.com/1b2435ee-4682-4499-aa5c-35201ab2ba95">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="https://msdn.microsoft.com/d67a85e7-6dfc-4444-bb69-a46e1234d021">IDynamicRenderer::DrawingAttributes Property</a>





## -see-also




<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

