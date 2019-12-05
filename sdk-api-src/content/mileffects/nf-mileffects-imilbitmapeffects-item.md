---
UID: NF:mileffects.IMILBitmapEffects.Item
title: IMILBitmapEffects::Item (mileffects.h)
description: Retrieves the effect at the given index.
old-location: wibe\_wibe_imilbitmapeffects_item.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\item.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffects interface [WPF Bitmap Effects],Item method, IMILBitmapEffects.Item, IMILBitmapEffects::Item, Item, Item method [WPF Bitmap Effects], Item method [WPF Bitmap Effects],IMILBitmapEffects interface, _wibe_imilbitmapeffects_item, mileffects/IMILBitmapEffects::Item, wibe._wibe_imilbitmapeffects_item
ms.topic: method
f1_keywords:
- mileffects/IMILBitmapEffects.Item
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.h
api_name:
- IMILBitmapEffects.Item
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffects::Item


## -description


Retrieves the effect at the given index.


## -parameters




### -param uindex

Type: <b>ULONG</b>

The index of the effect.


### -param ppEffect [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to the bitmap effect.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



