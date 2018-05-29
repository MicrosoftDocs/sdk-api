---
UID: NN:directmanipulation.IDirectManipulationCompositor
title: IDirectManipulationCompositor
author: windows-sdk-content
description: Represents a compositor object that associates manipulated content with a drawing surface, such as canvas (Windows app using JavaScript) or Canvas (Windows Store app using C++, C#, or Visual Basic).
old-location: directmanipulation\idirectmanipulationcompositor.htm
old-project: directmanipulation
ms.assetid: b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationCompositor, IDirectManipulationCompositor interface [Direct Manipulation], IDirectManipulationCompositor interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcompositor, directmanipulation/IDirectManipulationCompositor
ms.prod: windows
ms.technology: windows-sdk
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
-	IDirectManipulationCompositor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationCompositor interface


## -description



Represents a compositor object that associates manipulated content with a drawing surface, such as <a href="https://msdn.microsoft.com/642812b4-79da-4f16-834d-a00ea00cbfa3">canvas</a> (Windows app using JavaScript) or <a href="https://msdn.microsoft.com/cb84ddea-b812-4b4d-9c9c-12a8b1132afb">Canvas</a> (Windows Store app using C++, C#, or Visual Basic).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationCompositor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationCompositor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationCompositor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16c1a911-43cb-4c18-9e29-12a69b715e6a">AddContent</a>
</td>
<td align="left" width="63%">
Associates content (owned by the caller) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Commits all pending updates in the compositor to the system for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bfb7fe4-abf9-4bb7-8d3f-673508053573">RemoveContent</a>
</td>
<td align="left" width="63%">
Removes content from the compositor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8efab95b-2e06-4a3f-9b1b-171c1aada40a">SetUpdateManager</a>
</td>
<td align="left" width="63%">
    Sets the update manager used to send compositor updates to <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>. 

</td>
</tr>
</table> 


## -remarks



The content of a <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> viewport must be manually updated during an input event for custom implementations of <b>IDirectManipulationCompositor</b>. Call <a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a> to redraw the content within the viewport. 

You specify manual mode on a viewport by calling either of these functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions</a>, with <a href="https://msdn.microsoft.com/BFBA2D32-825F-4EEF-99C8-291305926750">DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE</a> specified.</li>
<li>
<a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a>, with <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> specified.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>



<a href="https://msdn.microsoft.com/e428ddaa-3913-498a-a3fd-bed10289cd8d">IDirectManipulationCompositor2</a>
 

 

