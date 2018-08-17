---
UID: NF:wincodecsdk.IWICMetadataReader.GetValue
title: IWICMetadataReader::GetValue
author: windows-sdk-content
description: Gets the metadata item value.
old-location: wic\_wic_codec_iwicmetadatareader_getvalue.htm
old-project: wic
ms.assetid: 7ae1328d-cda7-4522-9bcf-2c4b16fd6984
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetValue, GetValue method [Windows Imaging Component], GetValue method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetValue method, IWICMetadataReader.GetValue, IWICMetadataReader::GetValue, _wic_codec_iwicmetadatareader_getvalue, wic._wic_codec_iwicmetadatareader_getvalue, wincodecsdk/IWICMetadataReader::GetValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.redist: 
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
 - IWICMetadataReader.GetValue
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataReader::GetValue


## -description


Gets the metadata item value.


## -parameters




### -param pvarSchema [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the metadata item's schema property.


### -param pvarId [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the metadata item's id.


### -param pvarValue [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer that receives the metadata value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



