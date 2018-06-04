---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



