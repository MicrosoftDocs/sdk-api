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

# IStreamAsync::WriteAsync


## -description


Writes information to a stream asynchronously. For example, the Shell implements this method on file items when transferring them asynchronously.


## -parameters




### -param lpBuffer [in]

Type: <b>const void*</b>

A pointer to a buffer of size <i>cb</i> bytes that contains the information to be written to the stream.


### -param cb [in]

Type: <b>DWORD</b>

The size of the buffer pointed to by <i>lpBuffer</i>, in bytes.


### -param pcbWritten [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> value that, when the method returns successfully, states the actual number of bytes written to the stream. This value can be <b>NULL</b> if this information is not needed.


### -param lpOverlapped [in]

Type: <b>LPOVERLAPPED</b>

A pointer to an <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure that contains information used in the asynchronous write operation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>WriteAsync</b> should reset the event specified by the <b>hEvent</b> member of the <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure to a nonsignaled state when it begins the input/output (I/O) operation.



