---
UID: NF:wincodec.IWICDevelopRaw.GetWhitePointRGB
title: IWICDevelopRaw::GetWhitePointRGB
author: windows-sdk-content
description: Gets the white point RGB values.
old-location: wic\_wic_codec_iwicdevelopraw_getwhitepointrgb.htm
tech.root: wic
ms.assetid: e163ba80-6ed2-4f03-b74f-07c96b478ac0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetWhitePointRGB, GetWhitePointRGB method [Windows Imaging Component], GetWhitePointRGB method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetWhitePointRGB method, IWICDevelopRaw.GetWhitePointRGB, IWICDevelopRaw::GetWhitePointRGB, _wic_codec_iwicdevelopraw_getwhitepointrgb, wic._wic_codec_iwicdevelopraw_getwhitepointrgb, wincodec/IWICDevelopRaw::GetWhitePointRGB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.GetWhitePointRGB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::GetWhitePointRGB


## -description


Gets the white point RGB values.


## -parameters




### -param pRed [out]

Type: <b>UINT*</b>

A pointer that receives the red white point value.


### -param pGreen [out]

Type: <b>UINT*</b>

A pointer that receives the green white point value.


### -param pBlue [out]

Type: <b>UINT*</b>

A pointer that receives the blue white point value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



