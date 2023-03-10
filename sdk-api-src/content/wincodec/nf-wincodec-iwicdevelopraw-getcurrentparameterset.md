---
UID: NF:wincodec.IWICDevelopRaw.GetCurrentParameterSet
title: IWICDevelopRaw::GetCurrentParameterSet (wincodec.h)
description: Gets the current set of parameters.
helpviewer_keywords: ["GetCurrentParameterSet","GetCurrentParameterSet method [Windows Imaging Component]","GetCurrentParameterSet method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetCurrentParameterSet method","IWICDevelopRaw.GetCurrentParameterSet","IWICDevelopRaw::GetCurrentParameterSet","_wic_codec_iwicdevelopraw_getcurrentparameterset","wic._wic_codec_iwicdevelopraw_getcurrentparameterset","wincodec/IWICDevelopRaw::GetCurrentParameterSet"]
old-location: wic\_wic_codec_iwicdevelopraw_getcurrentparameterset.htm
tech.root: wic
ms.assetid: 06facc60-0d88-472d-827a-70e4006e947e
ms.date: 12/05/2018
ms.keywords: GetCurrentParameterSet, GetCurrentParameterSet method [Windows Imaging Component], GetCurrentParameterSet method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetCurrentParameterSet method, IWICDevelopRaw.GetCurrentParameterSet, IWICDevelopRaw::GetCurrentParameterSet, _wic_codec_iwicdevelopraw_getcurrentparameterset, wic._wic_codec_iwicdevelopraw_getcurrentparameterset, wincodec/IWICDevelopRaw::GetCurrentParameterSet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICDevelopRaw::GetCurrentParameterSet
 - wincodec/IWICDevelopRaw::GetCurrentParameterSet
dev_langs:
 - c++
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
---

# IWICDevelopRaw::GetCurrentParameterSet


## -description

Gets the current set of parameters.

## -parameters

### -param ppCurrentParameterSet [out]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>**</b>

A pointer that receives a pointer to the current set of parameters.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.