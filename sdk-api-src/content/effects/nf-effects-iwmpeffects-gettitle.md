---
UID: NF:effects.IWMPEffects.GetTitle
title: IWMPEffects::GetTitle (effects.h)
description: The GetTitle method gets the display title of the visualization.
helpviewer_keywords: ["EffectsGetTitle","GetTitle","GetTitle method [Windows Media Player]","GetTitle method [Windows Media Player]","IWMPEffects interface","IWMPEffects interface [Windows Media Player]","GetTitle method","IWMPEffects.GetTitle","IWMPEffects::GetTitle","effects/IWMPEffects::GetTitle","wmp.iwmpeffects_gettitle"]
old-location: wmp\iwmpeffects_gettitle.htm
tech.root: WMP
ms.assetid: 051a0d25-0773-4b9d-879e-5cc60633e406
ms.date: 12/05/2018
ms.keywords: EffectsGetTitle, GetTitle, GetTitle method [Windows Media Player], GetTitle method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetTitle method, IWMPEffects.GetTitle, IWMPEffects::GetTitle, effects/IWMPEffects::GetTitle, wmp.iwmpeffects_gettitle
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
 - IWMPEffects::GetTitle
 - effects/IWMPEffects::GetTitle
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
 - IWMPEffects.GetTitle
---

# IWMPEffects::GetTitle


## -description

The <b>GetTitle</b> method gets the display title of the visualization.

## -parameters

### -param bstrTitle [out]

<b>String</b> containing the title.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method allows the application to show the user a title when the visualization itself is displayed. The title should be as unique as possible. Do not use titles of visualizations included with the Windows Media Player as this will cause confusion to the user.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects">IWMPEffects Interface</a>