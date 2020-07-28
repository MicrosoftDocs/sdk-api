---
UID: NF:effects.IWMPEffects.GetPresetTitle
title: IWMPEffects::GetPresetTitle (effects.h)
description: The GetPresetTitle method gets the title of the current preset.
helpviewer_keywords: ["EffectsGetPresetTitle","GetPresetTitle","GetPresetTitle method [Windows Media Player]","GetPresetTitle method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GetPresetTitle method","IWMPEffects.GetPresetTitle","IWMPEffects::GetPresetTitle","effects/IWMPEffects::GetPresetTitle","wmp.iwmpeffects_getpresettitle"]
old-location: wmp\iwmpeffects_getpresettitle.htm
tech.root: WMP
ms.assetid: 73e80221-2170-4724-b902-5c30796cb6a4
ms.date: 12/05/2018
ms.keywords: EffectsGetPresetTitle, GetPresetTitle, GetPresetTitle method [Windows Media Player], GetPresetTitle method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetPresetTitle method, IWMPEffects.GetPresetTitle, IWMPEffects::GetPresetTitle, effects/IWMPEffects::GetPresetTitle, wmp.iwmpeffects_getpresettitle
f1_keywords:
- effects/IWMPEffects.GetPresetTitle
dev_langs:
- c++
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
- IWMPEffects.GetPresetTitle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEffects::GetPresetTitle


## -description



The <b>GetPresetTitle</b> method gets the title of the current preset.




## -parameters




### -param nPreset [in]

<b>Long</b> preset number.


### -param bstrPresetTitle [out]

<b>BSTR</b> preset title.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Called by Windows Media Player to obtain the title of a given preset.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>
 

 

