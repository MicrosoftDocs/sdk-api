---
UID: NF:mileffects.IMILBitmapEffectConnectorInfo.GetOptimalFormat
title: IMILBitmapEffectConnectorInfo::GetOptimalFormat (mileffects.h)
description: Retrieves the optimal pixel format for the pin.
helpviewer_keywords: ["GetOptimalFormat","GetOptimalFormat method [WPF Bitmap Effects]","GetOptimalFormat method [WPF Bitmap Effects]","IMILBitmapEffectConnectorInfo interface","IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects]","GetOptimalFormat method","IMILBitmapEffectConnectorInfo.GetOptimalFormat","IMILBitmapEffectConnectorInfo::GetOptimalFormat","_wibe_imilbitmapeffectconnectorinfo_getoptimalformat","mileffects/IMILBitmapEffectConnectorInfo::GetOptimalFormat","wibe._wibe_imilbitmapeffectconnectorinfo_getoptimalformat"]
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo_getoptimalformat.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\getoptimalformat.htm
ms.date: 12/05/2018
ms.keywords: GetOptimalFormat, GetOptimalFormat method [WPF Bitmap Effects], GetOptimalFormat method [WPF Bitmap Effects],IMILBitmapEffectConnectorInfo interface, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],GetOptimalFormat method, IMILBitmapEffectConnectorInfo.GetOptimalFormat, IMILBitmapEffectConnectorInfo::GetOptimalFormat, _wibe_imilbitmapeffectconnectorinfo_getoptimalformat, mileffects/IMILBitmapEffectConnectorInfo::GetOptimalFormat, wibe._wibe_imilbitmapeffectconnectorinfo_getoptimalformat
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
 - IMILBitmapEffectConnectorInfo::GetOptimalFormat
 - mileffects/IMILBitmapEffectConnectorInfo::GetOptimalFormat
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
 - IMILBitmapEffectConnectorInfo.GetOptimalFormat
---

# IMILBitmapEffectConnectorInfo::GetOptimalFormat


## -description

Retrieves the optimal pixel format for the pin.

## -parameters

### -param pFormat [out, retval]

Type: <b>WICPixelFormatGUID*</b>

When this method returns, contains the optimal pixel format for the pin.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

