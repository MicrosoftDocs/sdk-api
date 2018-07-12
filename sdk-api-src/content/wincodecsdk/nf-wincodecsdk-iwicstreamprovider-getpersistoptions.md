---
UID: NF:wincodecsdk.IWICStreamProvider.GetPersistOptions
title: IWICStreamProvider::GetPersistOptions
author: windows-sdk-content
description: Gets the persist options used when initializing the component with a stream.
old-location: wic\_wic_codec_iwicstreamprovider_getpersistoptions.htm
old-project: wic
ms.assetid: 244d4335-ee5f-434e-8d0b-4ba5d984b207
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetPersistOptions, GetPersistOptions method [Windows Imaging Component], GetPersistOptions method [Windows Imaging Component],IWICStreamProvider interface, IWICStreamProvider interface [Windows Imaging Component],GetPersistOptions method, IWICStreamProvider.GetPersistOptions, IWICStreamProvider::GetPersistOptions, _wic_codec_iwicstreamprovider_getpersistoptions, wic._wic_codec_iwicstreamprovider_getpersistoptions, wincodecsdk/IWICStreamProvider::GetPersistOptions
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
 - IWICStreamProvider.GetPersistOptions
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICStreamProvider::GetPersistOptions


## -description


Gets the persist options used when initializing the component with a stream.


## -parameters




### -param pdwPersistOptions [out]

Type: <b>DWORD*</b>

Pointer that receives the persist options used when initializing the component with a stream. If none were provided, <b>WICPersistOptionDefault</b> is returned.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



