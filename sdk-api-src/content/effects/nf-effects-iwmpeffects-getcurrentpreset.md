---
UID: NF:effects.IWMPEffects.GetCurrentPreset
title: IWMPEffects::GetCurrentPreset (effects.h)
description: The GetCurrentPreset method gets the current preset, by number, from the visualization and provides it to Windows Media Player.
helpviewer_keywords: ["EffectsGetCurrentPreset","GetCurrentPreset","GetCurrentPreset method [Windows Media Player]","GetCurrentPreset method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GetCurrentPreset method","IWMPEffects.GetCurrentPreset","IWMPEffects::GetCurrentPreset","effects/IWMPEffects::GetCurrentPreset","wmp.iwmpeffects_getcurrentpreset"]
old-location: wmp\iwmpeffects_getcurrentpreset.htm
tech.root: WMP
ms.assetid: 09ad671b-612d-4e00-8fa9-d9d76954a010
ms.date: 12/05/2018
ms.keywords: EffectsGetCurrentPreset, GetCurrentPreset, GetCurrentPreset method [Windows Media Player], GetCurrentPreset method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetCurrentPreset method, IWMPEffects.GetCurrentPreset, IWMPEffects::GetCurrentPreset, effects/IWMPEffects::GetCurrentPreset, wmp.iwmpeffects_getcurrentpreset
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEffects::GetCurrentPreset
 - effects/IWMPEffects::GetCurrentPreset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.GetCurrentPreset
---

# IWMPEffects::GetCurrentPreset


## -description

The <b>GetCurrentPreset</b> method gets the current preset, by number, from the visualization and provides it to Windows Media Player.

## -parameters

### -param pnPreset [in]

<b>Long</b> value specifying the current preset, by number.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>