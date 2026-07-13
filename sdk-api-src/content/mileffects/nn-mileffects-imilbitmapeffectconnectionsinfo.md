---
UID: NN:mileffects.IMILBitmapEffectConnectionsInfo
title: IMILBitmapEffectConnectionsInfo (mileffects.h)
description: Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect.
helpviewer_keywords: ["IMILBitmapEffectConnectionsInfo","IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects]","IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffectconnectionsinfo","mileffects/IMILBitmapEffectConnectionsInfo","wibe._wibe_imilbitmapeffectconnectionsinfo"]
old-location: wibe\_wibe_imilbitmapeffectconnectionsinfo.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectionsinfo\imilbitmapeffectconnectionsinfo.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnectionsInfo, IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects], IMILBitmapEffectConnectionsInfo interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectconnectionsinfo, mileffects/IMILBitmapEffectConnectionsInfo, wibe._wibe_imilbitmapeffectconnectionsinfo
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectConnectionsInfo
 - mileffects/IMILBitmapEffectConnectionsInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectConnectionsInfo
---

# IMILBitmapEffectConnectionsInfo interface


## -description

Exposes methods that retrieves information about what input and output pins are exposed by the bitmap effect.

## -inheritance

The <b>IMILBitmapEffectConnectionsInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectConnectionsInfo</b> also has these types of members:

## -remarks

If this interface is not implemented when creating a custom bitmap effect, a single input and output pin implementation with a 32bit RGBA format is assumes.
