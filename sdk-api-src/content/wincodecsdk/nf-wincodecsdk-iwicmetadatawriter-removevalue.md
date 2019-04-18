---
UID: NF:wincodecsdk.IWICMetadataWriter.RemoveValue
title: IWICMetadataWriter::RemoveValue (wincodecsdk.h)
author: windows-sdk-content
description: Removes the metadata item that matches the given parameters.
old-location: wic\_wic_codec_iwicmetadatawriter_removevalue.htm
tech.root: wic
ms.assetid: cc47b0d1-5772-4609-9696-816d39d04b34
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriter interface [Windows Imaging Component],RemoveValue method, IWICMetadataWriter.RemoveValue, IWICMetadataWriter::RemoveValue, RemoveValue, RemoveValue method [Windows Imaging Component], RemoveValue method [Windows Imaging Component],IWICMetadataWriter interface, _wic_codec_iwicmetadatawriter_removevalue, wic._wic_codec_iwicmetadatawriter_removevalue, wincodecsdk/IWICMetadataWriter::RemoveValue
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
 - IWICMetadataWriter.RemoveValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataWriter::RemoveValue


## -description


Removes the metadata item that matches the given parameters.


## -parameters




### -param pvarSchema [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the metadata schema property.


### -param pvarId [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the metadata id property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



