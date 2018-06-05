---
UID: NS:dwrite_3.DWRITE_FILE_FRAGMENT
title: DWRITE_FILE_FRAGMENT
author: windows-sdk-content
description: Represents a range of bytes in a font file.
old-location: directwrite\dwrite_file_fragment.htm
old-project: DirectWrite
ms.assetid: 6E893719-E2A7-482A-B344-8FE2AA59A6B9
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: DWRITE_FILE_FRAGMENT, DWRITE_FILE_FRAGMENT structure [Direct Write], directwrite.dwrite_file_fragment, dwrite_3/DWRITE_FILE_FRAGMENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dwrite_3.h
api_name:
-	DWRITE_FILE_FRAGMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_FILE_FRAGMENT structure


## -description


Represents a range of bytes in a font file.


## -struct-fields




### -field fileOffset

Starting offset of the fragment from the beginning of the file.


### -field fragmentSize

Size of the file fragment, in bytes.


## -remarks



DWRITE_FILE_FRAGMENT is passed as input to <a href="https://msdn.microsoft.com/A0EE8383-81A8-4974-B213-142704EFA210">IDWriteRemoteFontFileStream::BeginDownload</a>.



