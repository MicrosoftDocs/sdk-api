---
UID: NN:manipulations._IManipulationEvents
title: _IManipulationEvents (manipulations.h)
author: windows-sdk-content
description: Handles manipulation and inertia events.
old-location: wintouch\_imanipulationevents.htm
tech.root: wintouch
ms.assetid: be392a13-3165-44ff-bcd6-ed0075c669c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_IManipulationEvents, _IManipulationEvents interface [Windows Touch], _IManipulationEvents interface [Windows Touch],described, manipulations/_IManipulationEvents, wintouch._imanipulationevents"
ms.topic: interface
f1_keywords: ["manipulations/_IManipulationEvents"]
req.header: manipulations.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - _IManipulationEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IManipulationEvents interface


## -description


Handles manipulation and inertia events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">_IManipulationEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>_IManipulationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>_IManipulationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-_imanipulationevents-manipulationcompleted">ManipulationCompleted</a>
</td>
<td align="left" width="63%">
Handles the event when manipulation or inertia finishes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta">ManipulationDelta</a>
</td>
<td align="left" width="63%">
Handles events that happen when a manipulated object changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-_imanipulationevents-manipulationstarted">ManipulationStarted</a>
</td>
<td align="left" width="63%">
Handles the event when manipulation or inertia begins.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wintouch/intertmanip-classes-and-interfaces">Classes and Interfaces</a>
 

 

