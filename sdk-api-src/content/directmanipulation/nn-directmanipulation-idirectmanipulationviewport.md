---
UID: NN:directmanipulation.IDirectManipulationViewport
title: IDirectManipulationViewport
author: windows-driver-content
description: Defines a region within a window (referred to as a viewport) that is able to receive and process input from user interactions.
old-location: directmanipulation\idirectmanipulationviewport.htm
old-project: directmanipulation
ms.assetid: 4c14143b-3b5f-401d-9df7-f17374abcd99
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IDirectManipulationViewport, IDirectManipulationViewport interface [Direct Manipulation], IDirectManipulationViewport interface [Direct Manipulation],described, directmanipulation.idirectmanipulationviewport, directmanipulation/IDirectManipulationViewport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationViewport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport interface


## -description


Defines a region within a window (referred to as a viewport) that is able to receive and process input from user interactions.  The viewport contains content that moves in response to a user interaction. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationViewport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationViewport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/83d0bcde-03d2-4eba-991a-399b5307c8bd">Abandon</a>
</td>
<td align="left" width="63%">
    Releases all resources that are used by the viewport and prepares it for destruction from memory.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16c5902d-dddd-4c40-b1f9-cb432940aa3d">ActivateConfiguration</a>
</td>
<td align="left" width="63%">
Sets the configuration for input interaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/908f67ef-3606-4636-88aa-4e95d80a9c7a">AddConfiguration</a>
</td>
<td align="left" width="63%">
Adds an interaction configuration for the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c404e9a-832d-47af-b162-2783faa05237">AddContent</a>
</td>
<td align="left" width="63%">
Adds secondary content, such as a panning indicator, to a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56b47fec-dfa2-4906-9135-5ee331f04c54">AddEventHandler</a>
</td>
<td align="left" width="63%">
Adds a new event handler to listen for viewport events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh450971">Disable</a>
</td>
<td align="left" width="63%">
Stops input processing by the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">Enable</a>
</td>
<td align="left" width="63%">
Starts or resumes input processing by the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aa70be3-9e95-4c35-8cca-45c1b238961e">GetPrimaryContent</a>
</td>
<td align="left" width="63%">
Gets the primary content of a viewport that implements <a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a> and <a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the state of the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7523a99b-de43-4efe-ae22-6632167c039a">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag value of a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d20e7f7-aa2a-4c76-a3ff-da10d4dec3ea">GetViewportRect</a>
</td>
<td align="left" width="63%">
Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by <a href="https://msdn.microsoft.com/45dfdf6e-aa4d-489a-bf9a-016e42eb57f6">SetViewportRect</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ef43920-92bf-49c5-8e10-954d1b2b4440">ReleaseAllContacts</a>
</td>
<td align="left" width="63%">
Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbb5cfba-4722-4470-aad5-2d192825244b">ReleaseContact</a>
</td>
<td align="left" width="63%">
Removes a contact that is associated with a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2aac9468-a060-4f06-9e8e-139355be75f7">RemoveConfiguration</a>
</td>
<td align="left" width="63%">
Removes an interaction configuration for the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f7b709c-77ac-46fe-8fb5-dc4943824ab0">RemoveContent</a>
</td>
<td align="left" width="63%">
Removes secondary content from a viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea8539c0-2c0e-4259-a104-ecc02a46372a">RemoveEventHandler</a>
</td>
<td align="left" width="63%">
Removes an existing event handler from the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c172e985-4dc4-4d2a-a9e1-d88bc86ff75b">SetChaining</a>
</td>
<td align="left" width="63%">
Specifies the motion types supported in a viewport that can be chained to a parent viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39562bf1-c2cf-4ea6-9d02-a2b5fc4d3158">SetContact</a>
</td>
<td align="left" width="63%">
Specifies an  association between a contact and the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2be1c8a1-a729-4851-b103-b108b9a96e2d">SetInputMode</a>
</td>
<td align="left" width="63%">
Specifies if input is visible to the UI thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EBBBCEDB-8BAC-4E87-A69C-9730865A257F">SetManualGesture</a>
</td>
<td align="left" width="63%">
Sets which gestures are ignored by <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f695845b-8980-45cd-8231-e3ce29ce322f">SetTag</a>
</td>
<td align="left" width="63%">
Sets a viewport tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a>
</td>
<td align="left" width="63%">
    Specifies whether a viewport updates content manually instead of during an input event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions</a>
</td>
<td align="left" width="63%">
Sets how the viewport handles input and output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45dfdf6e-aa4d-489a-bf9a-016e42eb57f6">SetViewportRect</a>
</td>
<td align="left" width="63%">
    Sets the bounding rectangle for the viewport, relative to the origin of the viewport coordinate system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a35e0565-2833-45d3-b7dc-cf05bf644e96">SetViewportTransform</a>
</td>
<td align="left" width="63%">
Specifies the transform from the viewport coordinate system to the window client coordinate system. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
    Stops the manipulation and returns the viewport to a ready state.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0af63d1e-026e-4083-a1b2-56ba31653434">SyncDisplayTransform</a>
</td>
<td align="left" width="63%">
Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce87521d-bbce-43d3-920b-89eca101d260">ZoomToRect</a>
</td>
<td align="left" width="63%">
Moves the viewport to a specific area of the primary content and specifies whether to animate the transition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

