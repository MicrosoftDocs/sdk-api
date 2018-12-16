---
UID: NF:wincodec.IWICComponentInfo.GetVendorGUID
title: IWICComponentInfo::GetVendorGUID
author: windows-sdk-content
description: Retrieves the vendor GUID.
old-location: wic\_wic_codec_iwiccomponentinfo_getvendorguid.htm
tech.root: wic
ms.assetid: e1ef7bac-6845-4e7f-8cb6-bb3270b344d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVendorGUID, GetVendorGUID method [Windows Imaging Component], GetVendorGUID method [Windows Imaging Component],IWICComponentInfo interface, IWICComponentInfo interface [Windows Imaging Component],GetVendorGUID method, IWICComponentInfo.GetVendorGUID, IWICComponentInfo::GetVendorGUID, _wic_codec_iwiccomponentinfo_getvendorguid, wic._wic_codec_iwiccomponentinfo_getvendorguid, wincodec/IWICComponentInfo::GetVendorGUID
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICComponentInfo.GetVendorGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICComponentInfo::GetVendorGUID


## -description


Retrieves the vendor GUID.


## -parameters




### -param pguidVendor [out]

Type: <b>GUID*</b>

A pointer that receives the component's vendor GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



