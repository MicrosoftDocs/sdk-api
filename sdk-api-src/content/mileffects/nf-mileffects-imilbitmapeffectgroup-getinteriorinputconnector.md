---
UID: NF:mileffects.IMILBitmapEffectGroup.GetInteriorInputConnector
title: IMILBitmapEffectGroup::GetInteriorInputConnector (mileffects.h)
description: Retrieves the input connector for an effect at the given index.
old-location: wibe\_wibe_imilbitmapeffectgroup_getinteriorinputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\getinteriorinputconnector.htm
ms.date: 12/05/2018
ms.keywords: GetInteriorInputConnector, GetInteriorInputConnector method [WPF Bitmap Effects], GetInteriorInputConnector method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],GetInteriorInputConnector method, IMILBitmapEffectGroup.GetInteriorInputConnector, IMILBitmapEffectGroup::GetInteriorInputConnector, _wibe_imilbitmapeffectgroup_getinteriorinputconnector, mileffects/IMILBitmapEffectGroup::GetInteriorInputConnector, wibe._wibe_imilbitmapeffectgroup_getinteriorinputconnector
ms.topic: method
f1_keywords:
- mileffects/IMILBitmapEffectGroup.GetInteriorInputConnector
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
- IMILBitmapEffectGroup.GetInteriorInputConnector
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectGroup::GetInteriorInputConnector


## -description


Retrieves the input connector for an effect at the given index.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the effect to retrieve the connector.


### -param ppConnector [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a>**</b>

A pointer that receives a pointer to the desired effects input connector.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



