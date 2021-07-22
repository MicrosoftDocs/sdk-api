---
UID: NN:rtscom.IDynamicRenderer
title: IDynamicRenderer (rtscom.h)
description: Displays the tablet pen data in real-time as that data is being handled by the RealTimeStylus Class object.
helpviewer_keywords: ["6435b297-d6a7-418b-afc0-f8cc0b329842","IDynamicRenderer","IDynamicRenderer interface [Tablet PC]","IDynamicRenderer interface [Tablet PC]","described","rtscom/IDynamicRenderer","tablet.idynamicrenderer"]
old-location: tablet\idynamicrenderer.htm
tech.root: tablet
ms.assetid: 6435b297-d6a7-418b-afc0-f8cc0b329842
ms.date: 12/05/2018
ms.keywords: 6435b297-d6a7-418b-afc0-f8cc0b329842, IDynamicRenderer, IDynamicRenderer interface [Tablet PC], IDynamicRenderer interface [Tablet PC],described, rtscom/IDynamicRenderer, tablet.idynamicrenderer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDynamicRenderer
 - rtscom/IDynamicRenderer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer
---

# IDynamicRenderer interface


## -description

Displays the tablet pen data in real-time as that data is being handled by the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -inheritance

The <b>IDynamicRenderer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDynamicRenderer</b> also has these types of members:

## -remarks

This interface is implemented by the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>.

The <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> renders packet data dynamically.

Be sure the set the handle of the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> before you add it to a plug-in collection on the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>. If the handle is not set, the <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-error">IStylusPlugin::Error Method</a> notification method on each plug-in is called. For more information see <a href="/windows/desktop/tablet/error-handling-considerations-for-the-stylusinput-apis">Error Handling Considerations for the StylusInput APIs</a>.

The <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> implements the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> interface.

A <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> object can redraw the ink when a window has been invalidated.

While it is possible to have a given plug-in associated with multiple <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> objects, the <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> and <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> plug-ins are not designed to support this.

<div class="alert"><b>Note</b>  Calling interface members directly without the intervention of a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> instance is not supported.</div>
<div> </div>
The <a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a> has two categories of properties: those for which changes take effect immediately and those for which changes take effect upon the next <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a> event notification. The <a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a> property takes effect immediately, enabling the text input area to grow dynamically as the user writes. The other properties take effect after the next <b>IStylusPlugin::StylusDown Method</b> event notification.

The following are the properties for which changes take immediate effect:


<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_cliprectangle">IDynamicRenderer::ClipRectangle Property</a>


The following are the properties for which changes do not take immediate effect and are delayed:


<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_datacacheenabled">IDynamicRenderer::DataCacheEnabled Property</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-idynamicrenderer-get_drawingattributes">IDynamicRenderer::DrawingAttributes Property</a>

## -see-also

<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
