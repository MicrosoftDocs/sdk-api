---
UID: NF:wincodecsdk.IWICMetadataWriter.SetValue
title: IWICMetadataWriter::SetValue
author: windows-sdk-content
description: Sets the given metadata item.
old-location: wic\_wic_codec_iwicmetadatawriter_setvalue.htm
old-project: wic
ms.assetid: bda3f959-40d1-45df-a82c-3eba2be33859
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICMetadataWriter interface [Windows Imaging Component],SetValue method, IWICMetadataWriter.SetValue, IWICMetadataWriter::SetValue, SetValue, SetValue method [Windows Imaging Component], SetValue method [Windows Imaging Component],IWICMetadataWriter interface, _wic_codec_iwicmetadatawriter_setvalue, wic._wic_codec_iwicmetadatawriter_setvalue, wincodecsdk/IWICMetadataWriter::SetValue
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
 - IWICMetadataWriter.SetValue
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataWriter::SetValue


## -description


Sets the given metadata item.


## -parameters




### -param pvarSchema [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the schema property of the metadata item.


### -param pvarId [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the id property of the metadata item.


### -param pvarValue [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/Aa380072(v=VS.85).aspx">PROPVARIANT</a>*</b>

Pointer to the metadata value to set


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



