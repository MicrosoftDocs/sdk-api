---
UID: NF:effects.IWMPEffects.SetCurrentPreset
title: IWMPEffects::SetCurrentPreset
author: windows-sdk-content
description: The SetCurrentPreset method gets the current preset from Windows Media Player and sets it in the visualization.
old-location: wmp\iwmpeffects_setcurrentpreset.htm
tech.root: WMP
ms.assetid: 090e5f9b-e7f1-48b6-9018-3d0797493d42
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EffectsSetCurrentPreset, IWMPEffects interface [Windows Media Player],SetCurrentPreset method, IWMPEffects.SetCurrentPreset, IWMPEffects::SetCurrentPreset, SetCurrentPreset, SetCurrentPreset method [Windows Media Player], SetCurrentPreset method [Windows Media Player],IWMPEffects interface, effects/IWMPEffects::SetCurrentPreset, wmp.iwmpeffects_setcurrentpreset
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
 - IWMPEffects.SetCurrentPreset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEffects::SetCurrentPreset


## -description



The <b>SetCurrentPreset</b> method gets the current preset from Windows Media Player and sets it in the visualization.




## -parameters




### -param nPreset [out]

<b>Long</b> value specifying the new preset index.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This is called by the Windows Media Player to request that the given preset be displayed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563253(v=VS.85).aspx">IWMPEffects Interface</a>
 

 

