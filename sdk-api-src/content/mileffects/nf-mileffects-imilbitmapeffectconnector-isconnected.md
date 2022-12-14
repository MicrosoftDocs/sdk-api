---
UID: NF:mileffects.IMILBitmapEffectConnector.IsConnected
title: IMILBitmapEffectConnector::IsConnected (mileffects.h)
description: Determines whether the connector is connected to an effect.
helpviewer_keywords: ["IMILBitmapEffectConnector interface [WPF Bitmap Effects]","IsConnected method","IMILBitmapEffectConnector.IsConnected","IMILBitmapEffectConnector::IsConnected","IsConnected","IsConnected method [WPF Bitmap Effects]","IsConnected method [WPF Bitmap Effects]","IMILBitmapEffectConnector interface","_wibe_imilbitmapeffectconnector_isconnected","mileffects/IMILBitmapEffectConnector::IsConnected","wibe._wibe_imilbitmapeffectconnector_isconnected"]
old-location: wibe\_wibe_imilbitmapeffectconnector_isconnected.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnector\isconnected.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectConnector interface [WPF Bitmap Effects],IsConnected method, IMILBitmapEffectConnector.IsConnected, IMILBitmapEffectConnector::IsConnected, IsConnected, IsConnected method [WPF Bitmap Effects], IsConnected method [WPF Bitmap Effects],IMILBitmapEffectConnector interface, _wibe_imilbitmapeffectconnector_isconnected, mileffects/IMILBitmapEffectConnector::IsConnected, wibe._wibe_imilbitmapeffectconnector_isconnected
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
 - IMILBitmapEffectConnector::IsConnected
 - mileffects/IMILBitmapEffectConnector::IsConnected
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
 - IMILBitmapEffectConnector.IsConnected
---

# IMILBitmapEffectConnector::IsConnected


## -description

Determines whether the connector is connected to an effect.

## -parameters

### -param pfConnected [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer that receives <code>TRUE</code> if the connector is connected to an effect; otherwise, <code>FALSE</code>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

