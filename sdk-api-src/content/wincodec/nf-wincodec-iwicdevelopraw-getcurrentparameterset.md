---
UID: NF:wincodec.IWICDevelopRaw.GetCurrentParameterSet
title: IWICDevelopRaw::GetCurrentParameterSet
author: windows-sdk-content
description: Gets the current set of parameters.
old-location: wic\_wic_codec_iwicdevelopraw_getcurrentparameterset.htm
tech.root: wic
ms.assetid: 06facc60-0d88-472d-827a-70e4006e947e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetCurrentParameterSet, GetCurrentParameterSet method [Windows Imaging Component], GetCurrentParameterSet method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetCurrentParameterSet method, IWICDevelopRaw.GetCurrentParameterSet, IWICDevelopRaw::GetCurrentParameterSet, _wic_codec_iwicdevelopraw_getcurrentparameterset, wic._wic_codec_iwicdevelopraw_getcurrentparameterset, wincodec/IWICDevelopRaw::GetCurrentParameterSet
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.GetCurrentParameterSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICDevelopRaw::GetCurrentParameterSet


## -description


Gets the current set of parameters.


## -parameters




### -param ppCurrentParameterSet [out]

Type: <b><a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>**</b>

A pointer that receives a pointer to the current set of parameters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



