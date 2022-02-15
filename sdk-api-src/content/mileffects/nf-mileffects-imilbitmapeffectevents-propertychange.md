---
UID: NF:mileffects.IMILBitmapEffectEvents.PropertyChange
title: IMILBitmapEffectEvents::PropertyChange (mileffects.h)
description: Notifies an IMILBitmapEffectPrimitive of a property change.
helpviewer_keywords: ["IMILBitmapEffectEvents interface [WPF Bitmap Effects]","PropertyChange method","IMILBitmapEffectEvents.PropertyChange","IMILBitmapEffectEvents::PropertyChange","PropertyChange","PropertyChange method [WPF Bitmap Effects]","PropertyChange method [WPF Bitmap Effects]","IMILBitmapEffectEvents interface","_wibe_imilbitmapeffectevents_propertychange","mileffects/IMILBitmapEffectEvents::PropertyChange","wibe._wibe_imilbitmapeffectevents_propertychange"]
old-location: wibe\_wibe_imilbitmapeffectevents_propertychange.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectevents\propertychange.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectEvents interface [WPF Bitmap Effects],PropertyChange method, IMILBitmapEffectEvents.PropertyChange, IMILBitmapEffectEvents::PropertyChange, PropertyChange, PropertyChange method [WPF Bitmap Effects], PropertyChange method [WPF Bitmap Effects],IMILBitmapEffectEvents interface, _wibe_imilbitmapeffectevents_propertychange, mileffects/IMILBitmapEffectEvents::PropertyChange, wibe._wibe_imilbitmapeffectevents_propertychange
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
 - IMILBitmapEffectEvents::PropertyChange
 - mileffects/IMILBitmapEffectEvents::PropertyChange
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
 - IMILBitmapEffectEvents.PropertyChange
---

# IMILBitmapEffectEvents::PropertyChange


## -description

Notifies an <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectprimitive">IMILBitmapEffectPrimitive</a> of a property change.

## -parameters

### -param pEffect [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>*</b>

The effect primitive to notify.

### -param bstrPropertyName [in]

Type: <b>BSTR</b>

The property that has changed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.