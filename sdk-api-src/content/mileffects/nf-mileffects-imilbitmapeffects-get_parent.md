---
UID: NF:mileffects.IMILBitmapEffects.get_Parent
title: IMILBitmapEffects::get_Parent (mileffects.h)
description: Retrieves the parent effect group of enumeration.
helpviewer_keywords: ["IMILBitmapEffects interface [WPF Bitmap Effects]","get_Parent method","IMILBitmapEffects.get_Parent","IMILBitmapEffects::get_Parent","_wibe_imilbitmapeffects_parent","get_Parent","get_Parent method [WPF Bitmap Effects]","get_Parent method [WPF Bitmap Effects]","IMILBitmapEffects interface","mileffects/IMILBitmapEffects::get_Parent","wibe._wibe_imilbitmapeffects_parent"]
old-location: wibe\_wibe_imilbitmapeffects_parent.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffects\parent.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffects interface [WPF Bitmap Effects],get_Parent method, IMILBitmapEffects.get_Parent, IMILBitmapEffects::get_Parent, _wibe_imilbitmapeffects_parent, get_Parent, get_Parent method [WPF Bitmap Effects], get_Parent method [WPF Bitmap Effects],IMILBitmapEffects interface, mileffects/IMILBitmapEffects::get_Parent, wibe._wibe_imilbitmapeffects_parent
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
 - IMILBitmapEffects::get_Parent
 - mileffects/IMILBitmapEffects::get_Parent
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
 - IMILBitmapEffects.get_Parent
---

# IMILBitmapEffects::get_Parent


## -description

Retrieves the parent effect group of enumeration.

## -parameters

### -param ppEffect [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectgroup">IMILBitmapEffectGroup</a>**</b>

A pointer that receives a pointer to the parent group.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.