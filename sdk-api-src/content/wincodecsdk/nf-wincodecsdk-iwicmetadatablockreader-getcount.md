---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetCount
title: IWICMetadataBlockReader::GetCount (wincodecsdk.h)
description: Retrieves the number of top level metadata blocks.
old-location: wic\_wic_codec_iwicmetadatablockreader_getcount.htm
tech.root: wic
ms.assetid: 212e2376-9fad-4bfc-8883-ce89d05c35e6
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Imaging Component], GetCount method [Windows Imaging Component],IWICMetadataBlockReader interface, IWICMetadataBlockReader interface [Windows Imaging Component],GetCount method, IWICMetadataBlockReader.GetCount, IWICMetadataBlockReader::GetCount, _wic_codec_iwicmetadatablockreader_getcount, wic._wic_codec_iwicmetadatablockreader_getcount, wincodecsdk/IWICMetadataBlockReader::GetCount
f1_keywords:
- wincodecsdk/IWICMetadataBlockReader.GetCount
dev_langs:
- c++
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
- IWICMetadataBlockReader.GetCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataBlockReader::GetCount


## -description


Retrieves the number of top level metadata blocks.


## -parameters




### -param pcCount [out]

Type: <b>UINT*</b>

When this method returns, contains the number of top level metadata blocks.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>
 

 

