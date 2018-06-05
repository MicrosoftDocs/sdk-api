---
UID: NF:wincodecsdk.IWICMetadataReader.GetEnumerator
title: IWICMetadataReader::GetEnumerator
author: windows-sdk-content
description: Gets an enumerator of all the metadata items.
old-location: wic\_wic_codec_iwicmetadatareader_getenumerator.htm
old-project: wic
ms.assetid: 8dfb2b8d-2825-470e-8adc-85437d8fe863
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataReader.GetEnumerator, IWICMetadataReader::GetEnumerator, _wic_codec_iwicmetadatareader_getenumerator, wic._wic_codec_iwicmetadatareader_getenumerator, wincodecsdk/IWICMetadataReader::GetEnumerator
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICMetadataReader.GetEnumerator
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataReader::GetEnumerator


## -description


Gets an enumerator of all the metadata items.


## -parameters




### -param ppIEnumMetadata [out]

Type: <b><a href="https://msdn.microsoft.com/4fe0e47f-9ef4-4aa1-a3ae-578b3759f9ef">IWICEnumMetadataItem</a>**</b>

Pointer that receives a pointer to the metadata enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



