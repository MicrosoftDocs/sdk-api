---
UID: NF:effects.IWMPEffects2.Destroy
title: IWMPEffects2::Destroy (effects.h)
description: The Destroy method is called by Windows Media Player to destroy a visualization window instantiated in the Create method.
helpviewer_keywords: ["Destroy","Destroy method [Windows Media Player]","Destroy method [Windows Media Player]","IWMPEffects2 interface","IWMPEffects2 interface [Windows Media Player]","Destroy method","IWMPEffects2.Destroy","IWMPEffects2::Destroy","IWMPEffectsDestroy","effects/IWMPEffects2::Destroy","wmp.iwmpeffects2_destroy"]
old-location: wmp\iwmpeffects2_destroy.htm
tech.root: WMP
ms.assetid: dad290e6-a3be-47f0-a893-7a60eebc2a64
ms.date: 4/26/2023
ms.keywords: Destroy, Destroy method [Windows Media Player], Destroy method [Windows Media Player],IWMPEffects2 interface, IWMPEffects2 interface [Windows Media Player],Destroy method, IWMPEffects2.Destroy, IWMPEffects2::Destroy, IWMPEffectsDestroy, effects/IWMPEffects2::Destroy, wmp.iwmpeffects2_destroy
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
 - IWMPEffects2::Destroy
 - effects/IWMPEffects2::Destroy
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
 - IWMPEffects2.Destroy
---

# IWMPEffects2::Destroy


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Destroy</b> method is called by Windows Media Player to destroy a visualization window instantiated in the <b>Create</b> method.



## -returns

This method returns an <b>HRESULT</b>.

## -remarks

This method is used only by windowed visualizations. Windowless visualizations should simply return S_OK.

## -see-also

<a href="/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>



<a href="/windows/desktop/api/effects/nf-effects-iwmpeffects2-create">IWMPEffects2::Create</a>
