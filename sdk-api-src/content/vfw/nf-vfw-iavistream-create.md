---
UID: NF:vfw.IAVIStream.Create
title: IAVIStream::Create
author: windows-sdk-content
description: The Create method initializes a stream handler that is not associated with any file. Called when an application uses the AVIStreamCreate function.
old-location: multimedia\iavistream_create.htm
tech.root: Multimedia
ms.assetid: 512ce9f8-f96c-4ef4-be1f-234165219ff7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Create, Create method [Windows Multimedia], Create method [Windows Multimedia],IAVIStream interface, IAVIStream interface [Windows Multimedia],Create method, IAVIStream.Create, IAVIStream::Create, _win32_IAVIStream_Create, multimedia.iavistream_create, vfw/IAVIStream::Create
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStream.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::Create


## -description



The <b>Create</b> method initializes a stream handler that is not associated with any file. Called when an application uses the <a href="https://msdn.microsoft.com/8c784875-dc8f-4fd4-b267-0194cdbfa3c7">AVIStreamCreate</a> function.




## -parameters




### -param lParam1

Stream handler-specific data.


### -param lParam2

Stream handler-specific data.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Create</b> has the following syntax:


```cpp

HRESULT Create(LONG lParam1, LONG lParam2) 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

