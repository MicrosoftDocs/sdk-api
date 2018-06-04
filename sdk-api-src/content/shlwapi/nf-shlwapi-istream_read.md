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

# IStream_Read function


## -description


Reads bytes from a specified stream and returns a value that indicates whether all bytes were successfully read.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream from which to read.


### -param pv [out]

Type: <b>VOID*</b>

A pointer to a buffer to receive the stream data from <i>pstm</i>. This buffer must be at least <i>cb</i> bytes in size.


### -param cb [in]

Type: <b>ULONG</b>

The number of bytes of data that the function should attempt to read from the input stream.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the function successfully reads the specified number of bytes from the stream, or a COM failure code otherwise. In particular, if the read attempt was successful but fewer than <i>cb</i> bytes were read, the function returns <b>E_FAIL</b>.




## -remarks



This function calls the <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> method to read data from the specified stream into the buffer. If the function fails for any reason, the contents of the output buffer and the position of the read pointer in the input stream are undefined.





## -see-also




<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a>
 

 

