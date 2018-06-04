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

# IStreamAsync::ReadAsync


## -description


Reads information from a stream asynchronously. For example, the Shell implements this interface on file items when transferring them asynchronously.


## -parameters




### -param pv [out]

Type: <b>void*</b>

When this method returns successfully, returns a buffer that is <i>cb</i> bytes long and contains <i>pcbRead</i> bytes of information from the read operation.


### -param cb [in]

Type: <b>DWORD</b>

The number of bytes to read from the stream.


### -param pcbRead [out, optional]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> value that, when this method returns successfully, states the actual number of bytes read to the buffer pointed to by <i>pv</i>. This value can be <b>NULL</b>.


### -param lpOverlapped [in]

Type: <b>LPOVERLAPPED</b>

A pointer to an <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure that contains information used in the asynchronous read operation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IStreamAsync::ReadAsync</b> should reset the event specified by the <b>hEvent</b> member of the <a href="https://msdn.microsoft.com/2b5964e5-dfc8-44f9-86a7-5ea5acc68c1b">OVERLAPPED</a> structure to a nonsignaled state when it begins the input/output (I/O) operation.

This method has been implemented in the Shell as a thin wrapper around the public <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> API.



