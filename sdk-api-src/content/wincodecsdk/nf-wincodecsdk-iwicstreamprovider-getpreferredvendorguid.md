---
UID: NF:wincodecsdk.IWICStreamProvider.GetPreferredVendorGUID
title: IWICStreamProvider::GetPreferredVendorGUID (wincodecsdk.h)
description: Gets the preferred vendor GUID.
helpviewer_keywords: ["GetPreferredVendorGUID","GetPreferredVendorGUID method [Windows Imaging Component]","GetPreferredVendorGUID method [Windows Imaging Component]","IWICStreamProvider interface","IWICStreamProvider interface [Windows Imaging Component]","GetPreferredVendorGUID method","IWICStreamProvider.GetPreferredVendorGUID","IWICStreamProvider::GetPreferredVendorGUID","_wic_codec_iwicstreamprovider_getpreferredvendorguid","wic._wic_codec_iwicstreamprovider_getpreferredvendorguid","wincodecsdk/IWICStreamProvider::GetPreferredVendorGUID"]
old-location: wic\_wic_codec_iwicstreamprovider_getpreferredvendorguid.htm
tech.root: wic
ms.assetid: fb88bc8d-4f92-4645-9d11-ee9200f11aaf
ms.date: 12/05/2018
ms.keywords: GetPreferredVendorGUID, GetPreferredVendorGUID method [Windows Imaging Component], GetPreferredVendorGUID method [Windows Imaging Component],IWICStreamProvider interface, IWICStreamProvider interface [Windows Imaging Component],GetPreferredVendorGUID method, IWICStreamProvider.GetPreferredVendorGUID, IWICStreamProvider::GetPreferredVendorGUID, _wic_codec_iwicstreamprovider_getpreferredvendorguid, wic._wic_codec_iwicstreamprovider_getpreferredvendorguid, wincodecsdk/IWICStreamProvider::GetPreferredVendorGUID
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
 - IWICStreamProvider::GetPreferredVendorGUID
 - wincodecsdk/IWICStreamProvider::GetPreferredVendorGUID
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
 - IWICStreamProvider.GetPreferredVendorGUID
---

# IWICStreamProvider::GetPreferredVendorGUID


## -description

Gets the preferred vendor GUID.

## -parameters

### -param pguidPreferredVendor [out]

Type: <b>GUID*</b>

Pointer that receives the preferred vendor GUID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

