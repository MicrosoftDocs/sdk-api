---
UID: NN:rtscom.IDynamicRenderer
title: IDynamicRenderer (rtscom.h)
author: windows-sdk-content
description: Displays the tablet pen data in real-time as that data is being handled by the RealTimeStylus Class object.
old-location: tablet\idynamicrenderer.htm
tech.root: tablet
ms.assetid: 6435b297-d6a7-418b-afc0-f8cc0b329842
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6435b297-d6a7-418b-afc0-f8cc0b329842, IDynamicRenderer, IDynamicRenderer interface [Tablet PC], IDynamicRenderer interface [Tablet PC],described, rtscom/IDynamicRenderer, tablet.idynamicrenderer
ms.topic: interface
f1_keywords: 
 - "rtscom/IDynamicRenderer"
req.header: rtscom.h
req.include-header: 
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDynamicRenderer interface


## -description



Displays the tablet pen data in real-time as that data is being handled by the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDynamicRenderer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDynamicRenderer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-draw">Draw</a>
</td>
<td align="left" width="63%">
Draws the cached data to the specified device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Makes the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object refresh the data that it's currently rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">ReleaseCachedData</a>
</td>
<td align="left" width="63%">
Releases specified stroke data from the temporal data held by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object.

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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">ClipRectangle</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_clipregion">ClipRegion</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">DataCacheEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Allows the caller to specify whether to use the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-releasecacheddata">IDynamicRenderer::ReleaseCachedData Method</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">DrawingAttributes</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a> object used by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object. Allows the caller to set or modify the drawing attributes for the next stroke. Device rendering should not be using the <b>DynamicRenderer Class</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_enabled">Enabled</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_hwnd">HWND</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_hwnd">IDynamicRenderer::HWND Property</a> associated with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object. Defaults to <b>NULL</b>

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> renders packet data dynamically.

Be sure the set the handle of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> before you add it to a plug-in collection on the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>. If the handle is not set, the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-error">IStylusPlugin::Error Method</a> notification method on each plug-in is called. For more information see <a href="https://docs.microsoft.com/windows/desktop/tablet/error-handling-considerations-for-the-stylusinput-apis">Error Handling Considerations for the StylusInput APIs</a>.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> implements the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> interface.

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object can redraw the ink when a window has been invalidated.

While it is possible to have a given plug-in associated with multiple <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> objects, the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> and <a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> plug-ins are not designed to support this.

<div class="alert"><b>Note</b>  Calling interface members directly without the intervention of a <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> instance is not supported.</div>
<div> </div>
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> has two categories of properties: those for which changes take effect immediately and those for which changes take effect upon the next <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a> event notification. The <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a> property takes effect immediately, enabling the text input area to grow dynamically as the user writes. The other properties take effect after the next <b>IStylusPlugin::StylusDown Method</b> event notification.

The following are the properties for which changes take immediate effect:


<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a>


The following are the properties for which changes do not take immediate effect and are delayed:


<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
 

 

