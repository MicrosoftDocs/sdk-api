---
UID: NF:wincodec.IWICDevelopRaw.GetKelvinRangeInfo
title: IWICDevelopRaw::GetKelvinRangeInfo method
author: windows-driver-content
description: Gets the information about the current Kelvin range of the raw image.
old-location: wic\_wic_codec_iwicdevelopraw_getkelvinrangeinfo.htm
old-project: wic
ms.assetid: c718c957-3523-4281-aa7e-761977a6b4c5
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetKelvinRangeInfo method [Windows Imaging Component], GetKelvinRangeInfo method [Windows Imaging Component], IWICDevelopRaw interface, GetKelvinRangeInfo,IWICDevelopRaw.GetKelvinRangeInfo, IWICDevelopRaw, IWICDevelopRaw interface [Windows Imaging Component], GetKelvinRangeInfo method, IWICDevelopRaw::GetKelvinRangeInfo, _wic_codec_iwicdevelopraw_getkelvinrangeinfo, wic._wic_codec_iwicdevelopraw_getkelvinrangeinfo, wincodec/IWICDevelopRaw::GetKelvinRangeInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICDevelopRaw.GetKelvinRangeInfo
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::GetKelvinRangeInfo method


## -description


Gets the information about the current Kelvin range of the raw image.


## -parameters




### -param pMinKelvinTemp [out]

Type: <b>UINT*</b>

A pointer that receives the minimum Kelvin temperature.


### -param pMaxKelvinTemp [out]

Type: <b>UINT*</b>

A pointer that receives the maximum Kelvin temperature. 


### -param pKelvinTempStepValue [out]

Type: <b>UINT*</b>

A pointer that receives the Kelvin step value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



