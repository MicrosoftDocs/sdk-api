---
UID: NN:directmanipulation.IDirectManipulationInteractionEventHandler
title: IDirectManipulationInteractionEventHandler
author: windows-sdk-content
description: Defines methods to handle interactions when they are detected.
old-location: directmanipulation\idirectmanipulationinteractioneventhandler.htm
old-project: directmanipulation
ms.assetid: 9B832530-54B8-4D18-A5E4-4F4CAE65073A
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IDirectManipulationInteractionEventHandler, IDirectManipulationInteractionEventHandler interface [Direct Manipulation], IDirectManipulationInteractionEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationinteractioneventhandler, directmanipulation/IDirectManipulationInteractionEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
-	IDirectManipulationInteractionEventHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationInteractionEventHandler interface


## -description


Defines methods to handle interactions when they are detected.
<div class="alert"><b>Note</b>  When implementing this interface, ensure that the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff547910">InterlockedIncrement</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff547871">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationInteractionEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectManipulationInteractionEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationInteractionEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75822986-5691-4E2B-B6DB-A91D98B39BE8">OnInteraction</a>
</td>
<td align="left" width="63%">
Called when an interaction is detected.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>
 

 

