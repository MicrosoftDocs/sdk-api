---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.DoesRequireFixedSize
title: IWICMetadataHandlerInfo::DoesRequireFixedSize (wincodecsdk.h)
description: Determines if the metadata handler requires a fixed size.
helpviewer_keywords: ["DoesRequireFixedSize","DoesRequireFixedSize method [Windows Imaging Component]","DoesRequireFixedSize method [Windows Imaging Component]","IWICMetadataHandlerInfo interface","IWICMetadataHandlerInfo interface [Windows Imaging Component]","DoesRequireFixedSize method","IWICMetadataHandlerInfo.DoesRequireFixedSize","IWICMetadataHandlerInfo::DoesRequireFixedSize","_wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize","wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize","wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFixedSize"]
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize.htm
tech.root: wic
ms.assetid: 522294c5-e424-40cf-b982-275198e705dc
ms.date: 12/05/2018
ms.keywords: DoesRequireFixedSize, DoesRequireFixedSize method [Windows Imaging Component], DoesRequireFixedSize method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],DoesRequireFixedSize method, IWICMetadataHandlerInfo.DoesRequireFixedSize, IWICMetadataHandlerInfo::DoesRequireFixedSize, _wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize, wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefixedsize, wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFixedSize
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataHandlerInfo::DoesRequireFixedSize
 - wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFixedSize
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
 - IWICMetadataHandlerInfo.DoesRequireFixedSize
---

# IWICMetadataHandlerInfo::DoesRequireFixedSize


## -description

Determines if the metadata handler requires a fixed size.

## -parameters

### -param pfFixedSize [out]

Type: <b>BOOL*</b>

Pointer that receives <b>TRUE</b> if a fixed size is required; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

