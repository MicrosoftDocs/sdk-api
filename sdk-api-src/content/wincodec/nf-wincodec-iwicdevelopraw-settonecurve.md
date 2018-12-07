---
UID: NF:wincodec.IWICDevelopRaw.SetToneCurve
title: IWICDevelopRaw::SetToneCurve
author: windows-sdk-content
description: Sets the tone curve for the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_settonecurve.htm
tech.root: wic
ms.assetid: cfb0b67d-7eb1-4bbb-90be-33ca82b9460f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetToneCurve method, IWICDevelopRaw.SetToneCurve, IWICDevelopRaw::SetToneCurve, SetToneCurve, SetToneCurve method [Windows Imaging Component], SetToneCurve method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_settonecurve, wic._wic_codec_iwicdevelopraw_settonecurve, wincodec/IWICDevelopRaw::SetToneCurve
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
 - IWICDevelopRaw.SetToneCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::SetToneCurve


## -description


Sets the tone curve for the raw image.


## -parameters




### -param cbToneCurveSize [in]

Type: <b>UINT</b>

The size of the <i>pToneCurve</i> structure.


### -param pToneCurve [in]

Type: <b>const <a href="https://msdn.microsoft.com/45eedc32-a642-4ef6-a02a-63eaeacf0012">WICRawToneCurve</a>*</b>

The desired tone curve.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



