---
UID: NN:directmanipulation.IDirectManipulationUpdateHandler
title: IDirectManipulationUpdateHandler
author: windows-sdk-content
description: Defines methods for handling manipulation update events.
old-location: directmanipulation\idirectmanipulationupdatehandler.htm
old-project: directmanipulation
ms.assetid: a963abb5-63b8-44d1-910c-ea795398d3de
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationUpdateHandler, IDirectManipulationUpdateHandler interface [Direct Manipulation], IDirectManipulationUpdateHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatehandler, directmanipulation/IDirectManipulationUpdateHandler
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
-	IDirectManipulationUpdateHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationUpdateHandler interface


## -description



Defines methods for handling manipulation update events.


<div class="alert"><b>Note</b>  When implementing a <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> object, ensure that the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547910">InterlockedIncrement</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff547871">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationUpdateHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationUpdateHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationUpdateHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927294">Update</a>
</td>
<td align="left" width="63%">
Notifies the compositor when to update inertia animation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

