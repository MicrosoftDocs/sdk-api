---
UID: NF:wincodec.IWICImagingFactory.CreateQueryWriter
title: IWICImagingFactory::CreateQueryWriter
author: windows-sdk-content
description: Creates a new instance of a query writer.
old-location: wic\_wic_codec_iwicimagingfactory_createquerywriter.htm
old-project: wic
ms.assetid: c2998d22-68c5-45de-a651-6f67c6f5234a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CreateQueryWriter, CreateQueryWriter method [Windows Imaging Component], CreateQueryWriter method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateQueryWriter method, IWICImagingFactory.CreateQueryWriter, IWICImagingFactory::CreateQueryWriter, _wic_codec_iwicimagingfactory_createquerywriter, wic._wic_codec_iwicimagingfactory_createquerywriter, wincodec/IWICImagingFactory::CreateQueryWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICImagingFactory.CreateQueryWriter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICImagingFactory::CreateQueryWriter


## -description


Creates a new instance of a query writer.


## -parameters




### -param guidMetadataFormat [in]

Type: <b>REFGUID</b>

The GUID for the desired metadata format. 


### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred metadata writer vendor. Use <b>NULL</b> if no preferred vendor.


### -param ppIQueryWriter [out]

Type: <b><a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to a new <a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

