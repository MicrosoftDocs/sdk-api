---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.DoesRequireFullStream
title: IWICMetadataHandlerInfo::DoesRequireFullStream (wincodecsdk.h)
description: Determines if the handler requires a full stream.
helpviewer_keywords: ["DoesRequireFullStream","DoesRequireFullStream method [Windows Imaging Component]","DoesRequireFullStream method [Windows Imaging Component]","IWICMetadataHandlerInfo interface","IWICMetadataHandlerInfo interface [Windows Imaging Component]","DoesRequireFullStream method","IWICMetadataHandlerInfo.DoesRequireFullStream","IWICMetadataHandlerInfo::DoesRequireFullStream","_wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream","wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream","wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFullStream"]
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream.htm
tech.root: wic
ms.assetid: f434fd44-47a2-40be-ab3f-3d99b5e0e56a
ms.date: 12/05/2018
ms.keywords: DoesRequireFullStream, DoesRequireFullStream method [Windows Imaging Component], DoesRequireFullStream method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],DoesRequireFullStream method, IWICMetadataHandlerInfo.DoesRequireFullStream, IWICMetadataHandlerInfo::DoesRequireFullStream, _wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream, wic._wic_codec_iwicmetadatahandlerinfo_doesrequirefullstream, wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFullStream
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
 - IWICMetadataHandlerInfo::DoesRequireFullStream
 - wincodecsdk/IWICMetadataHandlerInfo::DoesRequireFullStream
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
 - IWICMetadataHandlerInfo.DoesRequireFullStream
---

# IWICMetadataHandlerInfo::DoesRequireFullStream


## -description

Determines if the handler requires a full stream.

## -parameters

### -param pfRequiresFullStream [out]

Type: <b>BOOL*</b>

Pointer that receives <b>TRUE</b> if a full stream is required; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

