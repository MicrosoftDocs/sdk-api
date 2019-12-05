---
UID: NN:directmanipulation.IDirectManipulationInteractionEventHandler
title: IDirectManipulationInteractionEventHandler (directmanipulation.h)
description: Defines methods to handle interactions when they are detected.
old-location: directmanipulation\idirectmanipulationinteractioneventhandler.htm
tech.root: directmanipulation
ms.assetid: 9B832530-54B8-4D18-A5E4-4F4CAE65073A
ms.date: 12/05/2018
ms.keywords: IDirectManipulationInteractionEventHandler, IDirectManipulationInteractionEventHandler interface [Direct Manipulation], IDirectManipulationInteractionEventHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationinteractioneventhandler, directmanipulation/IDirectManipulationInteractionEventHandler
ms.topic: interface
f1_keywords:
- directmanipulation/IDirectManipulationInteractionEventHandler
dev_langs:
- c++
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
- IDirectManipulationInteractionEventHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationInteractionEventHandler interface


## -description


Defines methods to handle interactions when they are detected.
<div class="alert"><b>Note</b>  When implementing this interface, ensure that the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockedincrement">InterlockedIncrement</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationInteractionEventHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationInteractionEventHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationinteractioneventhandler-oninteraction">OnInteraction</a>
</td>
<td align="left" width="63%">
Called when an interaction is detected.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

