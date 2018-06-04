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

# IPicture::SaveAsFile


## -description


Saves the picture's data into a stream in the same format that it would save itself into a file. Bitmaps use the BMP file format, metafiles the WMF format, and icons the ICO format.


## -parameters




### -param pStream [in]

A pointer to the stream into which the picture writes its data.


### -param fSaveMemCopy [in]

A flag indicating whether to save a copy of the picture in memory.


### -param pCbSize [out]

Pointer to a variable that receives the number of bytes written into the stream. This value can be <b>NULL</b>, indicating that the caller does not require this information.


## -returns



This method supports the standard return values E_FAIL, E_INVALIDARG, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

