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

# IStream_Write function


## -description


Writes data of unknown format from a buffer to a specified stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer that specifies the target stream.


### -param pv [in]

Type: <b>const void*</b>

Pointer to a buffer that holds the data to send to the target stream. This buffer must be at least <i>cb</i> bytes in size.


### -param cb [in]

Type: <b>ULONG</b>

The number of bytes of data to write to the target stream.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the function successfully wrote the specified number of bytes to the stream, or an error value otherwise. In particular, if less than <i>cb</i> bytes was written to the target stream, even if some data was successfully written, the function returns E_FAIL.



