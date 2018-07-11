---
UID: NF:wincodecsdk.IWICStreamProvider.GetPreferredVendorGUID
title: IWICStreamProvider::GetPreferredVendorGUID
author: windows-sdk-content
description: Gets the preferred vendor GUID.
old-location: wic\_wic_codec_iwicstreamprovider_getpreferredvendorguid.htm
old-project: wic
ms.assetid: fb88bc8d-4f92-4645-9d11-ee9200f11aaf
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetPreferredVendorGUID, GetPreferredVendorGUID method [Windows Imaging Component], GetPreferredVendorGUID method [Windows Imaging Component],IWICStreamProvider interface, IWICStreamProvider interface [Windows Imaging Component],GetPreferredVendorGUID method, IWICStreamProvider.GetPreferredVendorGUID, IWICStreamProvider::GetPreferredVendorGUID, _wic_codec_iwicstreamprovider_getpreferredvendorguid, wic._wic_codec_iwicstreamprovider_getpreferredvendorguid, wincodecsdk/IWICStreamProvider::GetPreferredVendorGUID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICPersistOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStreamProvider.GetPreferredVendorGUID
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



