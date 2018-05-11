---
UID: NF:wincodec.IWICBitmapDecoderInfo.GetPatterns
title: IWICBitmapDecoderInfo::GetPatterns
author: windows-driver-content
description: Retrieves the file pattern signatures supported by the decoder.
old-location: wic\_wic_codec_iwicbitmapdecoderinfo_getpatterns.htm
old-project: wic
ms.assetid: 6143a431-cea6-4ced-adf5-2aa4d90d622f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetPatterns, GetPatterns method [Windows Imaging Component], GetPatterns method [Windows Imaging Component],IWICBitmapDecoderInfo interface, IWICBitmapDecoderInfo interface [Windows Imaging Component],GetPatterns method, IWICBitmapDecoderInfo.GetPatterns, IWICBitmapDecoderInfo::GetPatterns, _wic_codec_iwicbitmapdecoderinfo_getpatterns, wic._wic_codec_iwicbitmapdecoderinfo_getpatterns, wincodec/IWICBitmapDecoderInfo::GetPatterns
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
-	IWICBitmapDecoderInfo.GetPatterns
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoderInfo::GetPatterns


## -description


Retrieves the file pattern signatures supported by the decoder.


## -parameters




### -param cbSizePatterns [in]

Type: <b>UINT</b>

The array size of the <i>pPatterns</i> array.


### -param pPatterns [out]

Type: <b><a href="https://msdn.microsoft.com/6f0cd639-c0db-46e4-b3a3-bc21222d97ee">WICBitmapPattern</a>*</b>

Receives a list of <a href="https://msdn.microsoft.com/6f0cd639-c0db-46e4-b3a3-bc21222d97ee">WICBitmapPattern</a> objects supported by the decoder.


### -param pcPatterns [out]

Type: <b>UINT*</b>

Receives the number of patterns the decoder supports.


### -param pcbPatternsActual [out]

Type: <b>UINT*</b>

Receives the actual buffer size needed to retrieve all pattern signatures supported by the decoder. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




               To retrieve all pattern signatures, this method should first be called with <i>pPatterns</i> set to <code>NULL</code> to retrieve the actual buffer size needed through <i>pcbPatternsActual</i>.
               Once the needed buffer size is known, allocate a buffer of the needed size and call <b>GetPatterns</b> again with the allocated buffer.
            



