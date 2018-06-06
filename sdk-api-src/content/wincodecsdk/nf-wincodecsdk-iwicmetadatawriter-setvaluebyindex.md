---
UID: NF:wincodecsdk.IWICMetadataWriter.SetValueByIndex
title: IWICMetadataWriter::SetValueByIndex
author: windows-sdk-content
description: Sets the metadata item to the specified index.
old-location: wic\_wic_codec_iwicmetadatawriter_setvaluebyindex.htm
old-project: wic
ms.assetid: 012ef661-c1cf-48fd-a748-223fa965f9a9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICMetadataWriter interface [Windows Imaging Component],SetValueByIndex method, IWICMetadataWriter.SetValueByIndex, IWICMetadataWriter::SetValueByIndex, SetValueByIndex, SetValueByIndex method [Windows Imaging Component], SetValueByIndex method [Windows Imaging Component],IWICMetadataWriter interface, _wic_codec_iwicmetadatawriter_setvaluebyindex, wic._wic_codec_iwicmetadatawriter_setvaluebyindex, wincodecsdk/IWICMetadataWriter::SetValueByIndex
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
 - IWICMetadataWriter.SetValueByIndex
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataWriter::SetValueByIndex


## -description


Sets the metadata item to the specified index.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

The index to place the metadata item.


### -param pvarSchema [in]

Type: <b>const <a href="_stg_propvariant">PROPVARIANT</a>*</b>

Pointer to the schema property of the metadata item.


### -param pvarId [in]

Type: <b>const <a href="_stg_propvariant">PROPVARIANT</a>*</b>

Pointer to the id property of the metadata item.


### -param pvarValue [in]

Type: <b>const <a href="_stg_propvariant">PROPVARIANT</a>*</b>

Pointer to the metadata value to set at the given index.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After removing an item, expect the remaining metadata items to move up to occupy the vacated metadata item location.  Therefore indices for remaining metadata items as well as the count will change.



