---
UID: NF:vfw.IAVIStream.SetFormat
title: IAVIStream::SetFormat
author: windows-driver-content
description: The SetFormat method sets format information in a stream. Called when an application uses the AVIStreamSetFormat function.
old-location: multimedia\iavistream_setformat.htm
old-project: Multimedia
ms.assetid: 8693ce01-1f73-4d1b-ba8a-12f6453def22
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAVIStream interface [Windows Multimedia],SetFormat method, IAVIStream.SetFormat, IAVIStream::SetFormat, SetFormat, SetFormat method [Windows Multimedia], SetFormat method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_SetFormat, multimedia.iavistream_setformat, vfw/IAVIStream::SetFormat
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
-	IAVIStream.SetFormat
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIStream::SetFormat


## -description



The <b>SetFormat</b> method sets format information in a stream. Called when an application uses the <a href="https://msdn.microsoft.com/b896f674-823d-49c9-8e48-c5081e37a13a">AVIStreamSetFormat</a> function.




## -parameters




### -param lPos




### -param lpFormat

Pointer to the buffer for the format data.


### -param cbFormat

Address containing the size, in bytes, of the buffer specified by <i>lpFormat</i>.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



Standard video stream handlers provide format information in a <b>BITMAPINFOHEADER</b> structure. Standard audio stream handlers provide format information in a <b>PCMWAVEFORMAT</b> structure. Other data streams can use other structures that describe the stream data.

For handlers written in C++, <b>SetFormat</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT SetFormat(LONG lPos, LPVOID lpFormat, LONG cbFormat) 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

