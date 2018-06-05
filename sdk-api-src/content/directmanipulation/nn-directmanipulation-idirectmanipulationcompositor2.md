---
UID: NN:directmanipulation.IDirectManipulationCompositor2
title: IDirectManipulationCompositor2
author: windows-sdk-content
description: Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.
old-location: directmanipulation\idirectmanipulationcompositor2.htm
old-project: directmanipulation
ms.assetid: e428ddaa-3913-498a-a3fd-bed10289cd8d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationCompositor2, IDirectManipulationCompositor2 interface [Direct Manipulation], IDirectManipulationCompositor2 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcompositor2, directmanipulation/IDirectManipulationCompositor2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DirectManipulation.h
api_name:
-	IDirectManipulationCompositor2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationCompositor2 interface


## -description


Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationCompositor2</b> interface inherits from <b>IDirectManipulationCompositor</b>. <b>IDirectManipulationCompositor2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationCompositor2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd6052df-30b5-4872-89a7-b98126fcd44d">AddContentWithCrossProcessChaining</a>
</td>
<td align="left" width="63%">
Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. 

</td>
</tr>
</table> 


## -remarks



The content of a <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> viewport must be manually updated during an input event for custom implementations of <b>IDirectManipulationCompositor2</b>. Call <a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a> to redraw the content within the viewport. 

You specify manual mode on a viewport by calling either of these functions:

<ul>
<li>
<a href="https://msdn.microsoft.com/F2B861B9-9E86-4AEE-B86C-03BF37F0988B">SetViewportOptions</a>, with <a href="https://msdn.microsoft.com/BFBA2D32-825F-4EEF-99C8-291305926750">DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE</a> specified.</li>
<li>
<a href="https://msdn.microsoft.com/10516474-f3ef-4de7-a5b5-aabaa5c65cf5">SetUpdateMode</a>, with <a href="https://msdn.microsoft.com/92839109-91d5-45fc-85d0-dc5a14e4ebf0">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> specified.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>



<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>
 

 

