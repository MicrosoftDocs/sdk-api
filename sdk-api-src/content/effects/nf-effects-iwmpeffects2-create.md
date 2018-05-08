---
UID: NF:effects.IWMPEffects2.Create
title: IWMPEffects2::Create
author: windows-driver-content
description: The Create method is called by Windows Media Player to instantiate a visualization window.
old-location: wmp\iwmpeffects2_create.htm
old-project: WMP
ms.assetid: a0bc4e45-7174-4dbd-a902-06c685c9a9ac
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: Create, Create method [Windows Media Player], Create method [Windows Media Player],IWMPEffects2 interface, IWMPEffects2 interface [Windows Media Player],Create method, IWMPEffects2.Create, IWMPEffects2::Create, IWMPEffectsCreate, effects/IWMPEffects2::Create, wmp.iwmpeffects2_create
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	effects.h
api_name:
-	IWMPEffects2.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects2::Create


## -description



The <b>Create</b> method is called by Windows Media Player to instantiate a visualization window.




## -parameters




### -param hwndParent [in]

<b>HWND</b> handle to the parent window hosting the visualization window.


## -returns



This method returns an <b>HRESULT</b>.




## -remarks



A visualization that implements <b>IWMPEffects2</b> is rendered in its own window unless it will be displayed in a clipped device context, in which case it is rendered windowless. For a visualization that is rendered windowless, Windows Media Player calls this method with a <b>NULL</b> value for the <i>hwndParent</i> parameter. If your visualization does not support windowless mode (for example, when using Direct3D), it should return a failure <b>HRESULT</b> value. In this case, your visualization will not be available in skins that clip the display region.

If you create a visualization for Windows Media Player using the Direct3D® component of Microsoft DirectX®, you must set the <b>D3DCREATE_FPU_PRESERVE</b> flag when calling <b>IDirect3D8::CreateDevice</b>. Failure to set this flag for visualizations that use Direct3D may yield unexpected results.




## -see-also




<a href="https://msdn.microsoft.com/44e044c1-97fd-43cb-9530-4556e485f5ae">IWMPEffects2 Interface</a>



<a href="https://msdn.microsoft.com/dad290e6-a3be-47f0-a893-7a60eebc2a64">IWMPEffects2::Destroy</a>
 

 

