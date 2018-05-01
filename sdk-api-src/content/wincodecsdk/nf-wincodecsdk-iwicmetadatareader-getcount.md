---
UID: NF:wincodecsdk.IWICMetadataReader.GetCount
title: IWICMetadataReader::GetCount method
author: windows-driver-content
description: Gets the number of metadata items within the reader.
old-location: wic\_wic_codec_iwicmetadatareader_getcount.htm
old-project: wic
ms.assetid: ce9b0267-112a-4aa9-8786-272ee4da4d8b
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetCount method [Windows Imaging Component], GetCount method [Windows Imaging Component], IWICMetadataReader interface, GetCount,IWICMetadataReader.GetCount, IWICMetadataReader, IWICMetadataReader interface [Windows Imaging Component], GetCount method, IWICMetadataReader::GetCount, _wic_codec_iwicmetadatareader_getcount, wic._wic_codec_iwicmetadatareader_getcount, wincodecsdk/IWICMetadataReader::GetCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICMetadataReader.GetCount
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataReader::GetCount method


## -description


Gets the number of metadata items within the reader.


## -parameters




### -param pcCount [out]

Type: <b>UINT*</b>

Pointer that receives the number of metadata items within the reader.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



