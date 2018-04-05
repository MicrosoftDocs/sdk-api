---
UID: NF:wincodec.IWICDdsDecoder.GetParameters
title: IWICDdsDecoder::GetParameters method
author: windows-driver-content
description: Gets DDS-specific data.
old-location: wic\iwicddsdecoder_getparameters.htm
old-project: wic
ms.assetid: D4EE39D6-54DC-450D-A430-2996D349BEC6
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: GetParameters method [Windows Imaging Component], GetParameters method [Windows Imaging Component], IWICDdsDecoder interface, GetParameters,IWICDdsDecoder.GetParameters, IWICDdsDecoder, IWICDdsDecoder interface [Windows Imaging Component], GetParameters method, IWICDdsDecoder::GetParameters, wic.iwicddsdecoder_getparameters, wincodec/IWICDdsDecoder::GetParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
-	IWICDdsDecoder.GetParameters
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDdsDecoder::GetParameters method


## -description


Gets DDS-specific data.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>*</b>

A pointer to the structure where the information is returned.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/632D1E7B-9C1D-48FB-95B5-1A295FE99577">IWICDdsDecoder</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

