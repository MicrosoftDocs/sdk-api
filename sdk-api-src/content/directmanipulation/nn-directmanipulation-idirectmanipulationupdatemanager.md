---
UID: NN:directmanipulation.IDirectManipulationUpdateManager
title: IDirectManipulationUpdateManager (directmanipulation.h)
description: Manages how compositor updates are sent to Direct Manipulation.
helpviewer_keywords: ["IDirectManipulationUpdateManager","IDirectManipulationUpdateManager interface [Direct Manipulation]","IDirectManipulationUpdateManager interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationupdatemanager","directmanipulation/IDirectManipulationUpdateManager"]
old-location: directmanipulation\idirectmanipulationupdatemanager.htm
tech.root: directmanipulation
ms.assetid: 30626a22-1ded-49ff-a6c3-619a14d5ee3b
ms.date: 12/05/2018
ms.keywords: IDirectManipulationUpdateManager, IDirectManipulationUpdateManager interface [Direct Manipulation], IDirectManipulationUpdateManager interface [Direct Manipulation],described, directmanipulation.idirectmanipulationupdatemanager, directmanipulation/IDirectManipulationUpdateManager
f1_keywords:
- directmanipulation/IDirectManipulationUpdateManager
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
- IDirectManipulationUpdateManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectManipulationUpdateManager interface


## -description


Manages how compositor updates are sent to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

This interface enables the compositor to trigger an update on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> whenever there is a compositor update. The application should not call the methods of this interface directly.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationUpdateManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationUpdateManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationUpdateManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-registerwaithandlecallback">RegisterWaitHandleCallback</a>
</td>
<td align="left" width="63%">
Registers a callback that is triggered by a handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-unregisterwaithandlecallback">UnregisterWaitHandleCallback</a>
</td>
<td align="left" width="63%">
Deregisters a callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-update">Update</a>
</td>
<td align="left" width="63%">
Updates <a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> at the current time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>
 

 

