---
UID: NF:vfw.IAVIStream.Write
title: IAVIStream::Write
author: windows-sdk-content
description: The Write method writes data to a stream. Called when an application uses the AVIStreamWrite function.
old-location: multimedia\iavistream_write.htm
tech.root: Multimedia
ms.assetid: 31252348-0830-4b1c-82a3-9f68818094da
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Write method, IAVIStream.Write, IAVIStream::Write, Write, Write method [Windows Multimedia], Write method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Write, multimedia.iavistream_write, vfw/IAVIStream::Write
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
 - IAVIStream.Write
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::Write


## -description



The <b>Write</b> method writes data to a stream. Called when an application uses the <a href="https://msdn.microsoft.com/9a306939-7b4f-4e0b-8340-270725da74c3">AVIStreamWrite</a> function.




## -parameters




### -param lStart

Starting sample or frame number to write.


### -param lSamples

Number of samples to write.


### -param lpBuffer

Pointer to the buffer for the data.


### -param cbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.


### -param dwFlags

Applicable flags. The AVIF_KEYFRAME flag is defined and indicates that this frame contains all the information needed for a complete image.


### -param plSampWritten

Pointer to a buffer used to contain the number of samples written.


### -param plBytesWritten

Pointer to a buffer that receives the number of bytes written.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Write</b> has the following syntax:


```cpp

HRESULT Write(LONG lStart, LONG lSamples, LPVOID lpBuffer, 
    LONG cbBuffer, DWORD dwFlags, LONG *plSampWritten, 
    LONG *plBytesWritten); 
 

```





## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

