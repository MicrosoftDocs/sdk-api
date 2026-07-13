---
UID: NN:mileffects.IMILBitmapEffectPrimitive
title: IMILBitmapEffectPrimitive (mileffects.h)
description: Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
helpviewer_keywords: ["IMILBitmapEffectPrimitive","IMILBitmapEffectPrimitive interface [WPF Bitmap Effects]","IMILBitmapEffectPrimitive interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffectprimitive","mileffects/IMILBitmapEffectPrimitive","wibe._wibe_imilbitmapeffectprimitive"]
old-location: wibe\_wibe_imilbitmapeffectprimitive.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\imilbitmapeffectprimitive.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitive, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects], IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitive, mileffects/IMILBitmapEffectPrimitive, wibe._wibe_imilbitmapeffectprimitive
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mileffects.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectPrimitive
 - mileffects/IMILBitmapEffectPrimitive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectPrimitive
---

# IMILBitmapEffectPrimitive interface


## -description

Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.

## -inheritance

The <b>IMILBitmapEffectPrimitive</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectPrimitive</b> also has these types of members:

## -remarks

Effect clients, in general, should interact with the outer <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> object rather than the <b>IMILBitmapEffectPrimitive</b> object.
            If the client needs to interact with the <b>IMILBitmapEffectPrimitive</b> directly the client will need to implement <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnections">IMILBitmapEffectConnections</a>, <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectionsinfo">IMILBitmapEffectConnectionsInfo</a>, and <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a>.
