---
UID: NE:wincodec.WICJpegIndexingOptions
title: WICJpegIndexingOptions
author: windows-driver-content
description: Specifies the options for indexing a JPEG image.
old-location: wic\wicjpegindexingoptions.htm
old-project: wic
ms.assetid: AFA9CC1B-847A-4237-9942-EC721FA86E4E
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: WICJpegIndexingOptions, WICJpegIndexingOptions enumeration [Windows Imaging Component], WICJpegIndexingOptionsGenerateOnDemand, WICJpegIndexingOptionsGenerateOnLoad, WICJpegIndexingOptions_FORCE_DWORD, wic.wicjpegindexingoptions, wincodec/WICJpegIndexingOptions, wincodec/WICJpegIndexingOptionsGenerateOnDemand, wincodec/WICJpegIndexingOptionsGenerateOnLoad, wincodec/WICJpegIndexingOptions_FORCE_DWORD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICJpegIndexingOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wincodec.h
api_name:
-	WICJpegIndexingOptions
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WICJpegIndexingOptions enumeration


## -description


Specifies the options for indexing a JPEG image. 


## -enum-fields




### -field WICJpegIndexingOptionsGenerateOnDemand

Index generation is deferred until <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a> is called on the image.


### -field WICJpegIndexingOptionsGenerateOnLoad

Index generation is performed when the when the image is initially loaded.


### -field WICJpegIndexingOptions_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -see-also




<a href="https://msdn.microsoft.com/D97A48E5-0398-460C-AFA9-2E1B8744926B">IWICJpegFrameDecode::SetIndexing</a>
 

 

