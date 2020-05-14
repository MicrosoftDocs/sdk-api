---
UID: NF:effects.IWMPEffects2.SetCore
title: IWMPEffects2::SetCore (effects.h)
description: The SetCore method is called by Windows Media Player to provide visualization access to the core Windows Media Player APIs.helpviewer_keywords: ["IWMPEffects2 interface [Windows Media Player]","SetCore method","IWMPEffects2.SetCore","IWMPEffects2::SetCore","IWMPEffectsSetCore","SetCore","SetCore method [Windows Media Player]","SetCore method [Windows Media Player]","IWMPEffects2 interface","effects/IWMPEffects2::SetCore","wmp.iwmpeffects2_setcore"]
old-location: wmp\iwmpeffects2_setcore.htm
tech.root: WMP
ms.assetid: d5afbf1d-ecb9-43d4-8396-db7c54720731
ms.date: 12/05/2018
ms.keywords: IWMPEffects2 interface [Windows Media Player],SetCore method, IWMPEffects2.SetCore, IWMPEffects2::SetCore, IWMPEffectsSetCore, SetCore, SetCore method [Windows Media Player], SetCore method [Windows Media Player],IWMPEffects2 interface, effects/IWMPEffects2::SetCore, wmp.iwmpeffects2_setcore
f1_keywords:
- effects/IWMPEffects2.SetCore
dev_langs:
- c++
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
- IWMPEffects2.SetCore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEffects2::SetCore


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/effects/nn-effects-iwmpeffects2">IWMPEffects2 Interface</a>
 

 

