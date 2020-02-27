---
UID: NN:directmanipulation.IDirectManipulationUpdateHandler
title: IDirectManipulationUpdateHandler (directmanipulation.h)
description: Defines methods for handling manipulation update events.
old-location: directmanipulation\idirectmanipulationupdatehandler.htm
tech.root: directmanipulation
ms.assetid: a963abb5-63b8-44d1-910c-ea795398d3de
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateHandler, IDirectManipulationUpdateHandler interface [Direct Manipulation], IDirectManipulationUpdateHandler interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatehandler, directmanipulation/IDirectManipulationUpdateHandler
f1_keywords:
- directmanipulation/IDirectManipulationUpdateHandler
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
- IDirectManipulationUpdateHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationUpdateHandler interface


## -description



Defines methods for handling manipulation update events.


<div class="alert"><b>Note</b>  When implementing a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> object, ensure that the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation supports multithreading through thread-safe reference counting. For more information, see <a href="/windows/win32/api/winnt/nf-winnt-interlockedincrement">InterlockedIncrement</a> and <a href="/windows/win32/api/winnt/nf-winnt-interlockeddecrement">InterlockedDecrement</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationUpdateHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationUpdateHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatehandler-update">Update</a>
</td>
<td align="left" width="63%">
Notifies the compositor when to update inertia animation.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

