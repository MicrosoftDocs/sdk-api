---
UID: NF:wincodec.IWICDevelopRaw.LoadParameterSet
title: IWICDevelopRaw::LoadParameterSet (wincodec.h)
description: Sets the desired WICRawParameterSet option.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","LoadParameterSet method","IWICDevelopRaw.LoadParameterSet","IWICDevelopRaw::LoadParameterSet","LoadParameterSet","LoadParameterSet method [Windows Imaging Component]","LoadParameterSet method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_loadparameterset","wic._wic_codec_iwicdevelopraw_loadparameterset","wincodec/IWICDevelopRaw::LoadParameterSet"]
old-location: wic\_wic_codec_iwicdevelopraw_loadparameterset.htm
tech.root: wic
ms.assetid: c3882d90-5772-4b10-8fcc-8d16f5004a05
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],LoadParameterSet method, IWICDevelopRaw.LoadParameterSet, IWICDevelopRaw::LoadParameterSet, LoadParameterSet, LoadParameterSet method [Windows Imaging Component], LoadParameterSet method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_loadparameterset, wic._wic_codec_iwicdevelopraw_loadparameterset, wincodec/IWICDevelopRaw::LoadParameterSet
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICDevelopRaw::LoadParameterSet
 - wincodec/IWICDevelopRaw::LoadParameterSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICDevelopRaw.LoadParameterSet
---

# IWICDevelopRaw::LoadParameterSet


## -description

Sets the desired <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawparameterset">WICRawParameterSet</a> option.

## -parameters

### -param ParameterSet [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawparameterset">WICRawParameterSet</a></b>

The desired <a href="/windows/desktop/api/wincodec/ne-wincodec-wicrawparameterset">WICRawParameterSet</a> option.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.