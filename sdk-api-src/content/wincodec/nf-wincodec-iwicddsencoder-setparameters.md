---
UID: NF:wincodec.IWICDdsEncoder.SetParameters
title: IWICDdsEncoder::SetParameters (wincodec.h)
description: Sets DDS-specific data.
helpviewer_keywords: ["IWICDdsEncoder interface [Windows Imaging Component]","SetParameters method","IWICDdsEncoder.SetParameters","IWICDdsEncoder::SetParameters","SetParameters","SetParameters method [Windows Imaging Component]","SetParameters method [Windows Imaging Component]","IWICDdsEncoder interface","wic.iwicddsencoder_setparameters","wincodec/IWICDdsEncoder::SetParameters"]
old-location: wic\iwicddsencoder_setparameters.htm
tech.root: wic
ms.assetid: 9DF51D95-97B0-4EC9-8F77-E49B16D76D77
ms.date: 12/05/2018
ms.keywords: IWICDdsEncoder interface [Windows Imaging Component],SetParameters method, IWICDdsEncoder.SetParameters, IWICDdsEncoder::SetParameters, SetParameters, SetParameters method [Windows Imaging Component], SetParameters method [Windows Imaging Component],IWICDdsEncoder interface, wic.iwicddsencoder_setparameters, wincodec/IWICDdsEncoder::SetParameters
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
 - IWICDdsEncoder::SetParameters
 - wincodec/IWICDdsEncoder::SetParameters
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
 - IWICDdsEncoder.SetParameters
---

# IWICDdsEncoder::SetParameters


## -description

Sets DDS-specific data.

## -parameters

### -param pParameters [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>*</b>

Points to the structure where the information is described.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You cannot call this method after you have started to write frame data, for example by calling <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe">IWICDdsEncoder::CreateNewFrame</a>.



Setting DDS parameters using this method provides the DDS encoder with information about the expected number of frames and the dimensions and other parameters of each frame. The DDS encoder will fail if you do not set frame data that matches these expectations. For example, if you set <a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters::Width</a> and <b>Height</b> to 32, and <b>MipLevels</b> to 6, the DDS encoder will expect 6 frames with the following dimensions:

<ul>
<li>32x32 pixels.</li>
<li>16x16 pixels.</li>
<li>8x8 pixels.</li>
<li>4x4 pixels.</li>
<li>2x2 pixels.</li>
<li>1x1 pixels.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder">IWICDdsEncoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicddsparameters">WICDdsParameters</a>