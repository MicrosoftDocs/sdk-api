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

# IWICStream::InitializeFromMemory


## -description


Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size. 


## -parameters




### -param pbBuffer [in]

Type: <b>BYTE*</b>

Pointer to the buffer used to initialize the stream.


### -param cbBufferSize [in]

Type: <b>DWORD</b>

The size of buffer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should be avoided whenever possible. The caller is responsible for ensuring the memory block is valid for the lifetime of the stream when using <b>InitializeFromMemory</b>.  A workaround for this behavior is to create an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> and use <a href="https://msdn.microsoft.com/bfe413e1-f579-4c9c-9e88-3b369235c529">InitializeFromIStream</a> to create the <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a>.

If you require a growable memory stream, use <a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a>.



