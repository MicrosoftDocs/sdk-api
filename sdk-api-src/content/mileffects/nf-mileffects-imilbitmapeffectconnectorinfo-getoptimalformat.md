---
UID: NF:mileffects.IMILBitmapEffectConnectorInfo.GetOptimalFormat
title: IMILBitmapEffectConnectorInfo::GetOptimalFormat method
author: windows-driver-content
description: Retrieves the optimal pixel format for the pin.
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo_getoptimalformat.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\getoptimalformat.htm
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetOptimalFormat method [WPF Bitmap Effects], GetOptimalFormat method [WPF Bitmap Effects], IMILBitmapEffectConnectorInfo interface, GetOptimalFormat,IMILBitmapEffectConnectorInfo.GetOptimalFormat, IMILBitmapEffectConnectorInfo, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects], GetOptimalFormat method, IMILBitmapEffectConnectorInfo::GetOptimalFormat, _wibe_imilbitmapeffectconnectorinfo_getoptimalformat, mileffects/IMILBitmapEffectConnectorInfo::GetOptimalFormat, wibe._wibe_imilbitmapeffectconnectorinfo_getoptimalformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectConnectorInfo.GetOptimalFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnectorInfo::GetOptimalFormat method


## -description


Retrieves the optimal pixel format for the pin.


## -parameters




### -param pFormat [out, retval]

Type: <b>WICPixelFormatGUID*</b>

When this method returns, contains the optimal pixel format for the pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



