---
UID: NF:wincodec.IWICDdsEncoder.GetParameters
title: IWICDdsEncoder::GetParameters (wincodec.h)
description: Gets DDS-specific data. (IWICDdsEncoder.GetParameters)
helpviewer_keywords: ["GetParameters","GetParameters method [Windows Imaging Component]","GetParameters method [Windows Imaging Component]","IWICDdsEncoder interface","IWICDdsEncoder interface [Windows Imaging Component]","GetParameters method","IWICDdsEncoder.GetParameters","IWICDdsEncoder::GetParameters","wic.iwicddsencoder_getparameters","wincodec/IWICDdsEncoder::GetParameters"]
old-location: wic\iwicddsencoder_getparameters.htm
tech.root: wic
ms.assetid: 2172A086-D0F6-4CFE-849C-A2EF1E89C050
ms.date: 12/05/2018
ms.keywords: GetParameters, GetParameters method [Windows Imaging Component], GetParameters method [Windows Imaging Component],IWICDdsEncoder interface, IWICDdsEncoder interface [Windows Imaging Component],GetParameters method, IWICDdsEncoder.GetParameters, IWICDdsEncoder::GetParameters, wic.iwicddsencoder_getparameters, wincodec/IWICDdsEncoder::GetParameters
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
 - IWICDdsEncoder::GetParameters
 - wincodec/IWICDdsEncoder::GetParameters
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
 - IWICDdsEncoder.GetParameters
---

# IWICDdsEncoder::GetParameters


## -description

Gets DDS-specific data.

## -parameters

### -param pParameters [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>*</b>

Points to the structure where the information is returned.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An application can call <b>GetParameters</b> to obtain the default DDS parameters, modify some or all of them, and then call <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters">SetParameters</a>.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder">IWICDdsEncoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>
