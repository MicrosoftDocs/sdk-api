---
UID: NF:mileffects.IMILBitmapEffectGroup.Add
title: IMILBitmapEffectGroup::Add (mileffects.h)
description: Adds an effect to the IMILBitmapEffectGroup.
helpviewer_keywords: ["Add","Add method [WPF Bitmap Effects]","Add method [WPF Bitmap Effects]","IMILBitmapEffectGroup interface","IMILBitmapEffectGroup interface [WPF Bitmap Effects]","Add method","IMILBitmapEffectGroup.Add","IMILBitmapEffectGroup::Add","_wibe_imilbitmapeffectgroup_add","mileffects/IMILBitmapEffectGroup::Add","wibe._wibe_imilbitmapeffectgroup_add"]
old-location: wibe\_wibe_imilbitmapeffectgroup_add.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\add.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [WPF Bitmap Effects], Add method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],Add method, IMILBitmapEffectGroup.Add, IMILBitmapEffectGroup::Add, _wibe_imilbitmapeffectgroup_add, mileffects/IMILBitmapEffectGroup::Add, wibe._wibe_imilbitmapeffectgroup_add
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
 - IMILBitmapEffectGroup::Add
 - mileffects/IMILBitmapEffectGroup::Add
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
 - IMILBitmapEffectGroup.Add
---

# IMILBitmapEffectGroup::Add


## -description

Adds an effect to the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectgroup">IMILBitmapEffectGroup</a>.

## -parameters

### -param pEffect [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>*</b>

A pointer to the effect to add to the group.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.