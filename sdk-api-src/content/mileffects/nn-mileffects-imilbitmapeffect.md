---
UID: NN:mileffects.IMILBitmapEffect
title: IMILBitmapEffect (mileffects.h)
description: Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.
helpviewer_keywords: ["IMILBitmapEffect","IMILBitmapEffect interface [WPF Bitmap Effects]","IMILBitmapEffect interface [WPF Bitmap Effects]","described","_wibe_imilbitmapeffect","mileffects/IMILBitmapEffect","wibe._wibe_imilbitmapeffect"]
old-location: wibe\_wibe_imilbitmapeffect.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffect\imilbitmapeffect.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffect, IMILBitmapEffect interface [WPF Bitmap Effects], IMILBitmapEffect interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffect, mileffects/IMILBitmapEffect, wibe._wibe_imilbitmapeffect
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
 - IMILBitmapEffect
 - mileffects/IMILBitmapEffect
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
 - IMILBitmapEffect
---

# IMILBitmapEffect interface


## -description

Exposes methods that define a Windows Presentation Foundation (WPF) bitmap effect.

## -inheritance

The <b>IMILBitmapEffect</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffect</b> also has these types of members:

## -remarks

<b>IMILBitmapEffect</b> is a wrapper for a <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a>. A <b>IMILBitmapEffectPrimitive</b> is wrapped by a <b>IMILBitmapEffect</b> through Component Object Model (COM) aggregation.
            Therefore, independent software vendor (ISV) effect writers do not need to implement the <b>IMILBitmapEffect</b>, <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectimpl">IMILBitmapEffectImpl</a>, and <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnections">IMILBitmapEffectConnections</a> interfaces.
