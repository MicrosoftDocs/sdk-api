---
UID: NF:ocidl.IPicture.SaveAsFile
title: IPicture::SaveAsFile
author: windows-sdk-content
description: Saves the picture's data into a stream in the same format that it would save itself into a file. Bitmaps use the BMP file format, metafiles the WMF format, and icons the ICO format.
old-location: com\ipicture_saveasfile.htm
old-project: com
ms.assetid: fa949064-d1cf-4056-9990-ae9ea88fae86
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPicture interface [COM],SaveAsFile method, IPicture.SaveAsFile, IPicture::SaveAsFile, SaveAsFile, SaveAsFile method [COM], SaveAsFile method [COM],IPicture interface, _ctrl_ipicture_saveasfile, com.ipicture_saveasfile, ocidl/IPicture::SaveAsFile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.SaveAsFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

