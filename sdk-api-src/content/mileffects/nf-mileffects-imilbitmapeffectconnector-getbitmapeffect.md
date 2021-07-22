---
UID: NF:mileffects.IMILBitmapEffectConnector.GetBitmapEffect
title: IMILBitmapEffectConnector::GetBitmapEffect (mileffects.h)
description: Gets the IMILBitmapEffect associated with the connector.
helpviewer_keywords: ["GetBitmapEffect","GetBitmapEffect method [WPF Bitmap Effects]","GetBitmapEffect method [WPF Bitmap Effects]","IMILBitmapEffectConnector interface","IMILBitmapEffectConnector interface [WPF Bitmap Effects]","GetBitmapEffect method","IMILBitmapEffectConnector.GetBitmapEffect","IMILBitmapEffectConnector::GetBitmapEffect","_wibe_imilbitmapeffectconnector_getbitmapeffect","mileffects/IMILBitmapEffectConnector::GetBitmapEffect","wibe._wibe_imilbitmapeffectconnector_getbitmapeffect"]
old-location: wibe\_wibe_imilbitmapeffectconnector_getbitmapeffect.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnector\getbitmapeffect.htm
ms.date: 12/05/2018
ms.keywords: GetBitmapEffect, GetBitmapEffect method [WPF Bitmap Effects], GetBitmapEffect method [WPF Bitmap Effects],IMILBitmapEffectConnector interface, IMILBitmapEffectConnector interface [WPF Bitmap Effects],GetBitmapEffect method, IMILBitmapEffectConnector.GetBitmapEffect, IMILBitmapEffectConnector::GetBitmapEffect, _wibe_imilbitmapeffectconnector_getbitmapeffect, mileffects/IMILBitmapEffectConnector::GetBitmapEffect, wibe._wibe_imilbitmapeffectconnector_getbitmapeffect
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
 - IMILBitmapEffectConnector::GetBitmapEffect
 - mileffects/IMILBitmapEffectConnector::GetBitmapEffect
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
 - IMILBitmapEffectConnector.GetBitmapEffect
---

# IMILBitmapEffectConnector::GetBitmapEffect


## -description

Gets the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> associated with the connector.

## -parameters

### -param ppEffect [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a>**</b>

A pointer that receives a pointer to the bitmap effect.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.