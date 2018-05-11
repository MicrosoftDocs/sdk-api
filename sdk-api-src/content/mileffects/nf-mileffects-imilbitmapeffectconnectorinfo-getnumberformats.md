---
UID: NF:mileffects.IMILBitmapEffectConnectorInfo.GetNumberFormats
title: IMILBitmapEffectConnectorInfo::GetNumberFormats
author: windows-driver-content
description: Retrieves the number of pixel formats supported by the pin.
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo_getnumberformats.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\getnumberformats.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetNumberFormats, GetNumberFormats method [WPF Bitmap Effects], GetNumberFormats method [WPF Bitmap Effects],IMILBitmapEffectConnectorInfo interface, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],GetNumberFormats method, IMILBitmapEffectConnectorInfo.GetNumberFormats, IMILBitmapEffectConnectorInfo::GetNumberFormats, _wibe_imilbitmapeffectconnectorinfo_getnumberformats, mileffects/IMILBitmapEffectConnectorInfo::GetNumberFormats, wibe._wibe_imilbitmapeffectconnectorinfo_getnumberformats
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
-	IMILBitmapEffectConnectorInfo.GetNumberFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectConnectorInfo::GetNumberFormats


## -description


Retrieves the number of pixel formats supported by the pin.


## -parameters




### -param pulNumberFormats [out, retval]

Type: <b>ULONG*</b>

When this method returns, contains the number of pixel formats supported by the pin.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



