---
UID: NF:mileffects.IMILBitmapEffectConnectorInfo.GetFormat
title: IMILBitmapEffectConnectorInfo::GetFormat (mileffects.h)
description: Retrieves the pixel format for the given pin.
helpviewer_keywords: ["GetFormat","GetFormat method [WPF Bitmap Effects]","GetFormat method [WPF Bitmap Effects]","IMILBitmapEffectConnectorInfo interface","IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects]","GetFormat method","IMILBitmapEffectConnectorInfo.GetFormat","IMILBitmapEffectConnectorInfo::GetFormat","_wibe_imilbitmapeffectconnectorinfo_getformat","mileffects/IMILBitmapEffectConnectorInfo::GetFormat","wibe._wibe_imilbitmapeffectconnectorinfo_getformat"]
old-location: wibe\_wibe_imilbitmapeffectconnectorinfo_getformat.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectconnectorinfo\getformat.htm
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [WPF Bitmap Effects], GetFormat method [WPF Bitmap Effects],IMILBitmapEffectConnectorInfo interface, IMILBitmapEffectConnectorInfo interface [WPF Bitmap Effects],GetFormat method, IMILBitmapEffectConnectorInfo.GetFormat, IMILBitmapEffectConnectorInfo::GetFormat, _wibe_imilbitmapeffectconnectorinfo_getformat, mileffects/IMILBitmapEffectConnectorInfo::GetFormat, wibe._wibe_imilbitmapeffectconnectorinfo_getformat
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
 - IMILBitmapEffectConnectorInfo::GetFormat
 - mileffects/IMILBitmapEffectConnectorInfo::GetFormat
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
 - IMILBitmapEffectConnectorInfo.GetFormat
---

# IMILBitmapEffectConnectorInfo::GetFormat


## -description

Retrieves the pixel format for the given pin.

## -parameters

### -param ulIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the pin to retrieve the pixel format.

### -param pFormat [out, retval]

Type: <b>WICPixelFormatGUID*</b>

When this method returns, contains the pixel format of the given pin.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

