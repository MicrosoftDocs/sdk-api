---
UID: NF:wincodecsdk.IWICPersistStream.LoadEx
title: IWICPersistStream::LoadEx
author: windows-sdk-content
description: Loads data from an input stream using the given parameters.
old-location: wic\_wic_codec_iwicpersiststream_loadex.htm
old-project: wic
ms.assetid: cb200a21-6c01-469e-b70f-f787f1dae382
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICPersistStream interface [Windows Imaging Component],LoadEx method, IWICPersistStream.LoadEx, IWICPersistStream::LoadEx, LoadEx, LoadEx method [Windows Imaging Component], LoadEx method [Windows Imaging Component],IWICPersistStream interface, _wic_codec_iwicpersiststream_loadex, wic._wic_codec_iwicpersiststream_loadex, wincodecsdk/IWICPersistStream::LoadEx
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
 - IWICPersistStream.LoadEx
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPersistStream::LoadEx


## -description


Loads data from an input stream using the given parameters.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Pointer to the input stream.


### -param pguidPreferredVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the preferred vendor .


### -param dwPersistOptions [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a> used to load the stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



NULL can be passed in for <i>pguidPreferredVendor</i> to indicate no preference.



