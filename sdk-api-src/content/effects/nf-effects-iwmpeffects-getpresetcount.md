---
UID: NF:effects.IWMPEffects.GetPresetCount
title: IWMPEffects::GetPresetCount (effects.h)
description: The GetPresetCount method gets the preset count.
helpviewer_keywords: ["EffectsGetPresetCount","GetPresetCount","GetPresetCount method [Windows Media Player]","GetPresetCount method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GetPresetCount method","IWMPEffects.GetPresetCount","IWMPEffects::GetPresetCount","effects/IWMPEffects::GetPresetCount","wmp.iwmpeffects_getpresetcount"]
old-location: wmp\iwmpeffects_getpresetcount.htm
tech.root: WMP
ms.assetid: 6eee859b-8f39-4951-814a-41913df152db
ms.date: 12/05/2018
ms.keywords: EffectsGetPresetCount, GetPresetCount, GetPresetCount method [Windows Media Player], GetPresetCount method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetPresetCount method, IWMPEffects.GetPresetCount, IWMPEffects::GetPresetCount, effects/IWMPEffects::GetPresetCount, wmp.iwmpeffects_getpresetcount
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
 - IWMPEffects::GetPresetCount
 - effects/IWMPEffects::GetPresetCount
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
 - IWMPEffects.GetPresetCount
---

# IWMPEffects::GetPresetCount


## -description

The <b>GetPresetCount</b> method gets the preset count.

## -parameters

### -param pnPresetCount [out]

<b>Long</b> value specifying the preset count.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Called by Windows Media Player to obtain the number of presets contained by the visualization.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>