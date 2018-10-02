---
UID: NF:wincodecsdk.IWICPersistStream.SaveEx
title: IWICPersistStream::SaveEx
author: windows-sdk-content
description: Saves the IWICPersistStream to the given input IStream using the given parameters.
old-location: wic\_wic_codec_iwicpersiststream_saveex.htm
tech.root: wic
ms.assetid: 8820ad87-a808-48db-91d8-c76bca1c832c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICPersistStream interface [Windows Imaging Component],SaveEx method, IWICPersistStream.SaveEx, IWICPersistStream::SaveEx, SaveEx, SaveEx method [Windows Imaging Component], SaveEx method [Windows Imaging Component],IWICPersistStream interface, _wic_codec_iwicpersiststream_saveex, wic._wic_codec_iwicpersiststream_saveex, wincodecsdk/IWICPersistStream::SaveEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPersistStream.SaveEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICPersistStream::SaveEx


## -description


Saves the <a href="https://msdn.microsoft.com/9381cc2c-9554-4071-b9b5-3464d857c02d">IWICPersistStream</a> to the given input <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> using the given parameters.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The stream to save to.


### -param dwPersistOptions [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a>  to use when saving.


### -param fClearDirty [in]

Type: <b>BOOL</b>

Indicates whether the "dirty" value will be cleared from all metadata after saving.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



