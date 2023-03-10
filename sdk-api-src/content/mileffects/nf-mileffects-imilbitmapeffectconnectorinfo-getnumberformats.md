---
UID: NF:mileffects.IMILBitmapEffectConnectorInfo.GetNumberFormats
title: IMILBitmapEffectConnectorInfo::GetNumberFormats (mileffects.h)
description: Retrieves the number of pixel formats supported by the pin.
helpviewer_keywords: ["GetNumberFormats","GetNumberFormats method [WPF Bitmap Effects]","GetNumberFormats method [WPF Bitmap Effects]","IMILBitmapEffectConnectorInfo interface","IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects]","GetNumberFormats method","IMILBitmapEffectConnectorInfo.GetNumberFormats","IMILBitmapEffectConnectorInfo::GetNumberFormats","_wibe_imilbitmapeffectconnectorinfo_getnumberformats","mileffects/IMILBitmapEffectConnectorInfo::GetNumberFormats","wibe._wibe_imilbitmapeffectconnectorinfo_getnumberformats"]
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo_getnumberformats.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\getnumberformats.htm
ms.date: 12/05/2018
ms.keywords: GetNumberFormats, GetNumberFormats method [WPF Bitmap Effects], GetNumberFormats method [WPF Bitmap Effects],IMILBitmapEffectConnectorInfo interface, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],GetNumberFormats method, IMILBitmapEffectConnectorInfo.GetNumberFormats, IMILBitmapEffectConnectorInfo::GetNumberFormats, _wibe_imilbitmapeffectconnectorinfo_getnumberformats, mileffects/IMILBitmapEffectConnectorInfo::GetNumberFormats, wibe._wibe_imilbitmapeffectconnectorinfo_getnumberformats
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
 - IMILBitmapEffectConnectorInfo::GetNumberFormats
 - mileffects/IMILBitmapEffectConnectorInfo::GetNumberFormats
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
 - IMILBitmapEffectConnectorInfo.GetNumberFormats
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

