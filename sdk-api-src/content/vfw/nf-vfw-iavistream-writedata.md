---
UID: NF:vfw.IAVIStream.WriteData
title: IAVIStream::WriteData
author: windows-sdk-content
description: The WriteData method writes headers for a stream. Called when an application uses the AVIStreamWriteData function.
old-location: multimedia\iavistream_writedata.htm
tech.root: Multimedia
ms.assetid: b6fb8e25-b6f9-4134-bb63-0a96fea88db8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAVIStream interface [Windows Multimedia],WriteData method, IAVIStream.WriteData, IAVIStream::WriteData, WriteData, WriteData method [Windows Multimedia], WriteData method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_WriteData, multimedia.iavistream_writedata, vfw/IAVIStream::WriteData
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
 - IAVIStream.WriteData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::WriteData


## -description



The <b>WriteData</b> method writes headers for a stream. Called when an application uses the <a href="https://msdn.microsoft.com/2ca91df6-4721-4282-8b88-81e76d2ab94f">AVIStreamWriteData</a> function.




## -parameters




### -param fcc

Four-character code of the stream header to write.


### -param lp

TBD


### -param cb

TBD




#### - cbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.


#### - lpBuffer

Pointer to the buffer that contains the header data to write.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>WriteData</b> has the following syntax:


```cpp

HRESULT WriteData(DWORD fcc, LPVOID lpBuffer, LONG cbBuffer); 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

