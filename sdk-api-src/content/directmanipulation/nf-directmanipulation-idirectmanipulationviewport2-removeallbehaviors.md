---
UID: NF:directmanipulation.IDirectManipulationViewport2.RemoveAllBehaviors
title: IDirectManipulationViewport2::RemoveAllBehaviors method
author: windows-driver-content
description: Removes all behaviors added to the viewport.
old-location: directmanipulation\idirectmanipulationviewport2_removeallbehaviors.htm
old-project: directmanipulation
ms.assetid: 94CCF2F4-F6E7-4446-8F6A-3E058B98A328
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDirectManipulationViewport2, IDirectManipulationViewport2 interface [Direct Manipulation], RemoveAllBehaviors method, IDirectManipulationViewport2::RemoveAllBehaviors, RemoveAllBehaviors method [Direct Manipulation], RemoveAllBehaviors method [Direct Manipulation], IDirectManipulationViewport2 interface, RemoveAllBehaviors,IDirectManipulationViewport2.RemoveAllBehaviors, directmanipulation.idirectmanipulationviewport2_removeallbehaviors, directmanipulation/IDirectManipulationViewport2::RemoveAllBehaviors
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IDirectManipulationViewport2.RemoveAllBehaviors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationViewport2::RemoveAllBehaviors method


## -description


Removes all behaviors added to the viewport.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>RemoveAllBehaviors</b> only returns an error if the removal of a behavior from the viewport was unsuccessful. In the event that a specific behavior is not removed successfully, <b>RemoveAllBehaviors</b> removes all remaining behaviors.




## -see-also




<a href="https://msdn.microsoft.com/6EDFBA93-D2A2-4089-9976-CD1F8421B319">IDirectManipulationViewport2</a>
 

 

