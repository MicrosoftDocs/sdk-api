---
UID: NF:vfw.IAVIStream.ReadFormat
title: IAVIStream::ReadFormat
author: windows-sdk-content
description: The ReadFormat method obtains format information from a stream.
old-location: multimedia\iavistream_readformat.htm
tech.root: Multimedia
ms.assetid: ec684a91-9a16-4e9d-9d52-8b721df24889
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAVIStream interface [Windows Multimedia],ReadFormat method, IAVIStream.ReadFormat, IAVIStream::ReadFormat, ReadFormat, ReadFormat method [Windows Multimedia], ReadFormat method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_ReadFormat, multimedia.iavistream_readformat, vfw/IAVIStream::ReadFormat
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
 - IAVIStream.ReadFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::ReadFormat


## -description



The <b>ReadFormat</b> method obtains format information from a stream. Fills and returns a structure with the data in an application-defined buffer. If no buffer is supplied, determines the buffer size needed to retrieve the buffer of format data. Called when an application uses the <a href="https://msdn.microsoft.com/312b7d20-89b2-4102-acf6-f603610dadd6">AVIStreamReadFormat</a> function.




## -parameters




### -param lPos

Position of the sample or frame.


### -param lpFormat

Pointer to the buffer for the format data. Specify <b>NULL</b> to request the required size of the buffer.


### -param lpcbFormat

Pointer to a buffer that receives the size, in bytes, of the buffer specified by <i>lpFormat</i>. When this method is called, the contents of this parameter indicates the size of the buffer specified by <i>lpFormat</i>. When this method returns control to the application, the contents of this parameter specifies the amount of data read or the required size of the buffer.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



The type of data stored in a stream dictates the format information and the structure that contains the format information. A stream handler should return all applicable format information in this structure, including palette information when the format uses a palette. A stream handler should not return stream data with the structure.

Standard video stream handlers provide format information in a <b>BITMAPINFOHEADER</b> structure. Standard audio stream handlers provide format information in a <b>PCMWAVEFORMAT</b> structure. Other data streams can use other structures that describe the stream data.

For handlers written in C++, <b>ReadFormat</b> has the following syntax:


```cpp

HRESULT ReadFormat(LONG lPos, LPVOID lpFormat, 
    LONG *lpcbFormat) 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

