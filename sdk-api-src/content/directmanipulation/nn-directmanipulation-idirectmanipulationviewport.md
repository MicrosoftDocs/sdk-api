---
UID: NN:directmanipulation.IDirectManipulationViewport
title: IDirectManipulationViewport (directmanipulation.h)
author: windows-sdk-content
description: Defines a region within a window (referred to as a viewport) that is able to receive and process input from user interactions.
old-location: directmanipulation\idirectmanipulationviewport.htm
tech.root: directmanipulation
ms.assetid: 4c14143b-3b5f-401d-9df7-f17374abcd99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectManipulationViewport, IDirectManipulationViewport interface [Direct Manipulation], IDirectManipulationViewport interface [Direct Manipulation],described, directmanipulation.idirectmanipulationviewport, directmanipulation/IDirectManipulationViewport
ms.topic: interface
f1_keywords: 
 - "directmanipulation/IDirectManipulationViewport"
dev_langs:
 - c++
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationViewport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationViewport interface


## -description


Defines a region within a window (referred to as a viewport) that is able to receive and process input from user interactions.  The viewport contains content that moves in response to a user interaction. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationViewport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationViewport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationViewport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-abandon">Abandon</a>
</td>
<td align="left" width="63%">
    Releases all resources that are used by the viewport and prepares it for destruction from memory.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration">ActivateConfiguration</a>
</td>
<td align="left" width="63%">
Sets the configuration for input interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration">AddConfiguration</a>
</td>
<td align="left" width="63%">
Adds an interaction configuration for the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addcontent">AddContent</a>
</td>
<td align="left" width="63%">
Adds secondary content, such as a panning indicator, to a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-addeventhandler">AddEventHandler</a>
</td>
<td align="left" width="63%">
Adds a new event handler to listen for viewport events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-disable">Disable</a>
</td>
<td align="left" width="63%">
Stops input processing by the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-enable">Enable</a>
</td>
<td align="left" width="63%">
Starts or resumes input processing by the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-getprimarycontent">GetPrimaryContent</a>
</td>
<td align="left" width="63%">
Gets the primary content of a viewport that implements <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the state of the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag value of a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-getviewportrect">GetViewportRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect">SetViewportRect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-releaseallcontacts">ReleaseAllContacts</a>
</td>
<td align="left" width="63%">
Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-releasecontact">ReleaseContact</a>
</td>
<td align="left" width="63%">
Removes a contact that is associated with a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeconfiguration">RemoveConfiguration</a>
</td>
<td align="left" width="63%">
Removes an interaction configuration for the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removecontent">RemoveContent</a>
</td>
<td align="left" width="63%">
Removes secondary content from a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-removeeventhandler">RemoveEventHandler</a>
</td>
<td align="left" width="63%">
Removes an existing event handler from the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setchaining">SetChaining</a>
</td>
<td align="left" width="63%">
Specifies the motion types supported in a viewport that can be chained to a parent viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact">SetContact</a>
</td>
<td align="left" width="63%">
Specifies an  association between a contact and the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setinputmode">SetInputMode</a>
</td>
<td align="left" width="63%">
Specifies if input is visible to the UI thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setmanualgesture">SetManualGesture</a>
</td>
<td align="left" width="63%">
Sets which gestures are ignored by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-settag">SetTag</a>
</td>
<td align="left" width="63%">
Sets a viewport tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setupdatemode">SetUpdateMode</a>
</td>
<td align="left" width="63%">
    Specifies whether a viewport updates content manually instead of during an input event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions</a>
</td>
<td align="left" width="63%">
Sets how the viewport handles input and output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect">SetViewportRect</a>
</td>
<td align="left" width="63%">
    Sets the bounding rectangle for the viewport, relative to the origin of the viewport coordinate system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewporttransform">SetViewportTransform</a>
</td>
<td align="left" width="63%">
Specifies the transform from the viewport coordinate system to the window client coordinate system. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-stop">Stop</a>
</td>
<td align="left" width="63%">
    Stops the manipulation and returns the viewport to a ready state.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform">SyncDisplayTransform</a>
</td>
<td align="left" width="63%">
Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-zoomtorect">ZoomToRect</a>
</td>
<td align="left" width="63%">
Moves the viewport to a specific area of the primary content and specifies whether to animate the transition.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

