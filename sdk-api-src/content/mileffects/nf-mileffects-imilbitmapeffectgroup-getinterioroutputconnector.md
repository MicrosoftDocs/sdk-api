---
UID: NF:mileffects.IMILBitmapEffectGroup.GetInteriorOutputConnector
title: IMILBitmapEffectGroup::GetInteriorOutputConnector (mileffects.h)
description: Retrieves the output connector for an effect at the given index.
helpviewer_keywords: ["GetInteriorOutputConnector","GetInteriorOutputConnector method [WPF Bitmap Effects]","GetInteriorOutputConnector method [WPF Bitmap Effects]","IMILBitmapEffectGroup interface","IMILBitmapEffectGroup interface [WPF Bitmap Effects]","GetInteriorOutputConnector method","IMILBitmapEffectGroup.GetInteriorOutputConnector","IMILBitmapEffectGroup::GetInteriorOutputConnector","_wibe_imilbitmapeffectgroup_getinterioroutputconnector","mileffects/IMILBitmapEffectGroup::GetInteriorOutputConnector","wibe._wibe_imilbitmapeffectgroup_getinterioroutputconnector"]
old-location: wibe\_wibe_imilbitmapeffectgroup_getinterioroutputconnector.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectgroup\getinterioroutputconnector.htm
ms.date: 12/05/2018
ms.keywords: GetInteriorOutputConnector, GetInteriorOutputConnector method [WPF Bitmap Effects], GetInteriorOutputConnector method [WPF Bitmap Effects],IMILBitmapEffectGroup interface, IMILBitmapEffectGroup interface [WPF Bitmap Effects],GetInteriorOutputConnector method, IMILBitmapEffectGroup.GetInteriorOutputConnector, IMILBitmapEffectGroup::GetInteriorOutputConnector, _wibe_imilbitmapeffectgroup_getinterioroutputconnector, mileffects/IMILBitmapEffectGroup::GetInteriorOutputConnector, wibe._wibe_imilbitmapeffectgroup_getinterioroutputconnector
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
 - IMILBitmapEffectGroup::GetInteriorOutputConnector
 - mileffects/IMILBitmapEffectGroup::GetInteriorOutputConnector
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
 - IMILBitmapEffectGroup.GetInteriorOutputConnector
---

# IMILBitmapEffectGroup::GetInteriorOutputConnector


## -description

Retrieves the output connector for an effect at the given index.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the effect to retrieve the connector.

### -param ppConnector [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectinputconnector">IMILBitmapEffectInputConnector</a>**</b>

A pointer that receives a pointer to the desired effects output connector.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.