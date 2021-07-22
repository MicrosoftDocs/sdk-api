---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.DoesSupportPadding
title: IWICMetadataHandlerInfo::DoesSupportPadding (wincodecsdk.h)
description: Determines if the metadata handler supports padding.
helpviewer_keywords: ["DoesSupportPadding","DoesSupportPadding method [Windows Imaging Component]","DoesSupportPadding method [Windows Imaging Component]","IWICMetadataHandlerInfo interface","IWICMetadataHandlerInfo interface [Windows Imaging Component]","DoesSupportPadding method","IWICMetadataHandlerInfo.DoesSupportPadding","IWICMetadataHandlerInfo::DoesSupportPadding","_wic_codec_iwicmetadatahandlerinfo_doessupportpadding","wic._wic_codec_iwicmetadatahandlerinfo_doessupportpadding","wincodecsdk/IWICMetadataHandlerInfo::DoesSupportPadding"]
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_doessupportpadding.htm
tech.root: wic
ms.assetid: 93f4e77a-52e3-47c7-9c48-9d38a2c8ceba
ms.date: 12/05/2018
ms.keywords: DoesSupportPadding, DoesSupportPadding method [Windows Imaging Component], DoesSupportPadding method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],DoesSupportPadding method, IWICMetadataHandlerInfo.DoesSupportPadding, IWICMetadataHandlerInfo::DoesSupportPadding, _wic_codec_iwicmetadatahandlerinfo_doessupportpadding, wic._wic_codec_iwicmetadatahandlerinfo_doessupportpadding, wincodecsdk/IWICMetadataHandlerInfo::DoesSupportPadding
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
 - IWICMetadataHandlerInfo::DoesSupportPadding
 - wincodecsdk/IWICMetadataHandlerInfo::DoesSupportPadding
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
 - IWICMetadataHandlerInfo.DoesSupportPadding
---

# IWICMetadataHandlerInfo::DoesSupportPadding


## -description

Determines if the metadata handler supports padding.

## -parameters

### -param pfSupportsPadding [out]

Type: <b>BOOL*</b>

Pointer that receives <b>TRUE</b> if padding is supported; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

