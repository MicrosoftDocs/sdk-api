---
UID: NF:wincodec.IWICDevelopRaw.LoadParameterSet
title: IWICDevelopRaw::LoadParameterSet method
author: windows-driver-content
description: Sets the desired WICRawParameterSet option.
old-location: wic\_wic_codec_iwicdevelopraw_loadparameterset.htm
old-project: wic
ms.assetid: c3882d90-5772-4b10-8fcc-8d16f5004a05
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IWICDevelopRaw, IWICDevelopRaw interface [Windows Imaging Component], LoadParameterSet method, IWICDevelopRaw::LoadParameterSet, LoadParameterSet method [Windows Imaging Component], LoadParameterSet method [Windows Imaging Component], IWICDevelopRaw interface, LoadParameterSet,IWICDevelopRaw.LoadParameterSet, _wic_codec_iwicdevelopraw_loadparameterset, wic._wic_codec_iwicdevelopraw_loadparameterset, wincodec/IWICDevelopRaw::LoadParameterSet
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
-	IWICDevelopRaw.LoadParameterSet
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICDevelopRaw::LoadParameterSet method


## -description


Sets the desired <a href="https://msdn.microsoft.com/0c39b769-9523-42ce-942f-761e6d39ec5b">WICRawParameterSet</a> option.


## -parameters




### -param ParameterSet [in]

Type: <b><a href="https://msdn.microsoft.com/0c39b769-9523-42ce-942f-761e6d39ec5b">WICRawParameterSet</a></b>

The desired <a href="https://msdn.microsoft.com/0c39b769-9523-42ce-942f-761e6d39ec5b">WICRawParameterSet</a> option.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



