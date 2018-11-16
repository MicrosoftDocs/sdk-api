---
UID: NF:effects.IWMPEffects2.Destroy
title: IWMPEffects2::Destroy
author: windows-sdk-content
description: The Destroy method is called by Windows Media Player to destroy a visualization window instantiated in the Create method.
old-location: wmp\iwmpeffects2_destroy.htm
tech.root: WMP
ms.assetid: dad290e6-a3be-47f0-a893-7a60eebc2a64
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Destroy, Destroy method [Windows Media Player], Destroy method [Windows Media Player],IWMPEffects2 interface, IWMPEffects2 interface [Windows Media Player],Destroy method, IWMPEffects2.Destroy, IWMPEffects2::Destroy, IWMPEffectsDestroy, effects/IWMPEffects2::Destroy, wmp.iwmpeffects2_destroy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
req.target-min-winversvr: 
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
 - effects.h
api_name:
 - IWMPEffects2.Destroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- effects.h
: 
- IWMPEffects2.Destroy
: 
---

# IWMPEffects2::Destroy


## -description



The <b>Destroy</b> method is called by Windows Media Player to destroy a visualization window instantiated in the <b>Create</b> method.




## -parameters






## -returns



This method returns an <b>HRESULT</b>.




## -remarks



This method is used only by windowed visualizations. Windowless visualizations should simply return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>



<a href="https://msdn.microsoft.com/a0bc4e45-7174-4dbd-a902-06c685c9a9ac">IWMPEffects2::Create</a>
 

 

