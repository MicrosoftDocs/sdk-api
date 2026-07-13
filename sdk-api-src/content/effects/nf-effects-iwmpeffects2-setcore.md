---
UID: NF:effects.IWMPEffects2.SetCore
title: IWMPEffects2::SetCore (effects.h)
description: The SetCore method is called by Windows Media Player to provide visualization access to the core Windows Media Player APIs.
helpviewer_keywords: ["IWMPEffects2 interface [Windows Media Player]","SetCore method","IWMPEffects2.SetCore","IWMPEffects2::SetCore","IWMPEffectsSetCore","SetCore","SetCore method [Windows Media Player]","SetCore method [Windows Media Player]","IWMPEffects2 interface","effects/IWMPEffects2::SetCore","wmp.iwmpeffects2_setcore"]
old-location: wmp\iwmpeffects2_setcore.htm
tech.root: WMP
ms.assetid: d5afbf1d-ecb9-43d4-8396-db7c54720731
ms.date: 4/26/2023
ms.keywords: IWMPEffects2 interface [Windows Media Player],SetCore method, IWMPEffects2.SetCore, IWMPEffects2::SetCore, IWMPEffectsSetCore, SetCore, SetCore method [Windows Media Player], SetCore method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::SetCore, wmp.iwmpeffects2_setcore
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEffects2::SetCore
 - effects/IWMPEffects2::SetCore
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
 - IWMPEffects2.SetCore
---

# IWMPEffects2::SetCore


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCore</b> method is called by Windows Media Player to provide visualization access to the core Windows Media Player APIs.

## -parameters

### -param pPlayer [in]

Pointer to an <b>IWMPCore</b> interface.

## -returns

This method returns an <b>HRESULT</b>.

## -remarks

You can use this method to set or release a pointer to the <b>IWMPCore</b> interface. If <i>pPlayer</i> is <b>NULL</b>, the visualization is being shut down and all stored references to the core should be released.

This method is not called when Windows Media Player instantiates the visualization for the purpose of displaying its property page. This method can therefore be used as an entry point that will only be called when the visualization is enabled and Windows Media Player loads it normally.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>