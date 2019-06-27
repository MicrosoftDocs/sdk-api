---
UID: NF:wincodecsdk.IWICMetadataWriter.RemoveValueByIndex
title: IWICMetadataWriter::RemoveValueByIndex (wincodecsdk.h)
author: windows-sdk-content
description: Removes the metadata item at the specified index.
old-location: wic\_wic_codec_iwicmetadatawriter_removevaluebyindex.htm
tech.root: wic
ms.assetid: 65cf7e21-e474-4652-9ee1-0802362f65ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriter interface [Windows Imaging Component],RemoveValueByIndex method, IWICMetadataWriter.RemoveValueByIndex, IWICMetadataWriter::RemoveValueByIndex, RemoveValueByIndex, RemoveValueByIndex method [Windows Imaging Component], RemoveValueByIndex method [Windows Imaging Component],IWICMetadataWriter interface, _wic_codec_iwicmetadatawriter_removevaluebyindex, wic._wic_codec_iwicmetadatawriter_removevaluebyindex, wincodecsdk/IWICMetadataWriter::RemoveValueByIndex
ms.topic: method
f1_keywords: 
 - "wincodecsdk/IWICMetadataWriter.RemoveValueByIndex"
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
 - IWICMetadataWriter.RemoveValueByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataWriter::RemoveValueByIndex


## -description


Removes the metadata item at the specified index.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata item to remove.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After removing an item, expect the remaining metadata items to move up to occupy the vacated metadata item location.  Therefore indices for remaining metadata items as well as the count will change.



