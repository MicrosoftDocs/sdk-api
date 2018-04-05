---
UID: NF:effects.IWMPEffects.GetCurrentPreset
title: IWMPEffects::GetCurrentPreset method
author: windows-driver-content
description: The GetCurrentPreset method gets the current preset, by number, from the visualization and provides it to Windows Media Player.
old-location: wmp\iwmpeffects_getcurrentpreset.htm
old-project: WMP
ms.assetid: 09ad671b-612d-4e00-8fa9-d9d76954a010
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: EffectsGetCurrentPreset, GetCurrentPreset method [Windows Media Player], GetCurrentPreset method [Windows Media Player], IWMPEffects interface, GetCurrentPreset,IWMPEffects.GetCurrentPreset, IWMPEffects, IWMPEffects interface [Windows Media Player], GetCurrentPreset method, IWMPEffects::GetCurrentPreset, effects/IWMPEffects::GetCurrentPreset, wmp.iwmpeffects_getcurrentpreset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
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
-	IWMPEffects.GetCurrentPreset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects::GetCurrentPreset method


## -description



The <b>GetCurrentPreset</b> method gets the current preset, by number, from the visualization and provides it to Windows Media Player.




## -parameters




### -param pnPreset






#### - currentpreset [in]

<b>Long</b> value specifying the current preset, by number.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

