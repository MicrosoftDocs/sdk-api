---
UID: NF:wincodec.IWICDevelopRaw.GetToneCurve
title: IWICDevelopRaw::GetToneCurve
author: windows-sdk-content
description: Gets the tone curve of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_gettonecurve.htm
tech.root: wic
ms.assetid: 651f9efb-145a-400b-8d7c-255aee67c385
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetToneCurve, GetToneCurve method [Windows Imaging Component], GetToneCurve method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetToneCurve method, IWICDevelopRaw.GetToneCurve, IWICDevelopRaw::GetToneCurve, _wic_codec_iwicdevelopraw_gettonecurve, wic._wic_codec_iwicdevelopraw_gettonecurve, wincodec/IWICDevelopRaw::GetToneCurve
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
 - IWICDevelopRaw.GetToneCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::GetToneCurve


## -description


Gets the tone curve of the raw image.


## -parameters




### -param cbToneCurveBufferSize [in]

Type: <b>UINT</b>

The size of the <i>pToneCurve</i> buffer.


### -param pToneCurve [out]

Type: <b><a href="https://msdn.microsoft.com/45eedc32-a642-4ef6-a02a-63eaeacf0012">WICRawToneCurve</a>*</b>

A pointer that receives the <a href="https://msdn.microsoft.com/45eedc32-a642-4ef6-a02a-63eaeacf0012">WICRawToneCurve</a> of the raw image.


### -param pcbActualToneCurveBufferSize [out]

Type: <b>UINT*</b>

A pointer that receives the size needed to obtain the tone curve structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



