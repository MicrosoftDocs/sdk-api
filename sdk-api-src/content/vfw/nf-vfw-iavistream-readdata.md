---
UID: NF:vfw.IAVIStream.ReadData
title: IAVIStream::ReadData
author: windows-sdk-content
description: The ReadData method reads data headers of a stream. Called when an application uses the AVIStreamReadData function.
old-location: multimedia\iavistream_readdata.htm
old-project: Multimedia
ms.assetid: 688a19fb-5774-4e05-b0e8-4a98922def89
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IAVIStream interface [Windows Multimedia],ReadData method, IAVIStream.ReadData, IAVIStream::ReadData, ReadData, ReadData method [Windows Multimedia], ReadData method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_ReadData, multimedia.iavistream_readdata, vfw/IAVIStream::ReadData
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IAVIStream.ReadData
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIStream::ReadData


## -description



The <b>ReadData</b> method reads data headers of a stream. Called when an application uses the <a href="https://msdn.microsoft.com/87a787e8-547a-4c35-ba65-a592bd037063">AVIStreamReadData</a> function.




## -parameters




### -param fcc

Four-character code of the stream header to read.


### -param lp




### -param lpcb






#### - lpBuffer

Pointer to the buffer to contain the header data.


#### - lpcbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>. When this method returns control to the application, the contents of this parameter specifies the amount of data read.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>ReadData</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT ReadData(DWORD fcc, LPVOID lp, LONG *lpcb); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

