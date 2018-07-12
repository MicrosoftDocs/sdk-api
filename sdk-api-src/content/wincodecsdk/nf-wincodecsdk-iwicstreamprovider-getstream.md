---
UID: NF:wincodecsdk.IWICStreamProvider.GetStream
title: IWICStreamProvider::GetStream
author: windows-sdk-content
description: Gets the stream held by the component.
old-location: wic\_wic_codec_iwicstreamprovider_getstream.htm
old-project: wic
ms.assetid: c86e507b-0b1d-4de0-8af5-c46d7870fb09
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetStream, GetStream method [Windows Imaging Component], GetStream method [Windows Imaging Component],IWICStreamProvider interface, IWICStreamProvider interface [Windows Imaging Component],GetStream method, IWICStreamProvider.GetStream, IWICStreamProvider::GetStream, _wic_codec_iwicstreamprovider_getstream, wic._wic_codec_iwicstreamprovider_getstream, wincodecsdk/IWICStreamProvider::GetStream
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
 - IWICStreamProvider.GetStream
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICStreamProvider::GetStream


## -description


Gets the stream held by the component.


## -parameters




### -param ppIStream [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

Pointer that receives a pointer to the stream held by the component.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



