---
UID: NF:wincodec.IWICDdsDecoder.GetParameters
title: IWICDdsDecoder::GetParameters (wincodec.h)
description: Gets DDS-specific data. (IWICDdsDecoder.GetParameters)
helpviewer_keywords: ["GetParameters","GetParameters method [Windows Imaging Component]","GetParameters method [Windows Imaging Component]","IWICDdsDecoder interface","IWICDdsDecoder interface [Windows Imaging Component]","GetParameters method","IWICDdsDecoder.GetParameters","IWICDdsDecoder::GetParameters","wic.iwicddsdecoder_getparameters","wincodec/IWICDdsDecoder::GetParameters"]
old-location: wic\iwicddsdecoder_getparameters.htm
tech.root: wic
ms.assetid: D4EE39D6-54DC-450D-A430-2996D349BEC6
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [Windows Imaging Component], GetParameters method [Windows Imaging Component],IWICDdsDecoder interface, IWICDdsDecoder interface [Windows Imaging Component],GetParameters method, IWICDdsDecoder.GetParameters, IWICDdsDecoder::GetParameters, wic.iwicddsdecoder_getparameters, wincodec/IWICDdsDecoder::GetParameters
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IWICDdsDecoder::GetParameters
 - wincodec/IWICDdsDecoder::GetParameters
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
 - IWICDdsDecoder.GetParameters
---

# IWICDdsDecoder::GetParameters


## -description

Gets DDS-specific data.

## -parameters

### -param pParameters [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>*</b>

A pointer to the structure where the information is returned.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder">IWICDdsDecoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>
