---
UID: NF:vfw.IAVIEditStream.Copy
title: IAVIEditStream::Copy
author: windows-sdk-content
description: The Copy method copies a stream or a portion of it to a temporary stream. Called when an application uses the EditStreamCopy function.
old-location: multimedia\iavieditstream_copy.htm
tech.root: Multimedia
ms.assetid: d2012d04-4fe5-4a49-8160-d27b7bc1bfc8
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: Copy, Copy method [Windows Multimedia], Copy method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Copy method, IAVIEditStream.Copy, IAVIEditStream::Copy, _win32_IAVIEditStream_Copy, multimedia.iavieditstream_copy, vfw/IAVIEditStream::Copy
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
 - IAVIEditStream.Copy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vfw.h
: 
- IAVIEditStream.Copy
: 
---

# IAVIEditStream::Copy


## -description



The <b>Copy</b> method copies a stream or a portion of it to a temporary stream. Called when an application uses the <a href="https://msdn.microsoft.com/c1548359-42ed-4d13-b72d-e7269a7c3482">EditStreamCopy</a> function.




## -parameters




### -param plStart

Pointer to a buffer that receives the starting position of the operation.


### -param plLength

Pointer to a buffer that receives the length, in frames, of the operation.


### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream to copy.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Copy</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Copy(LONG *plStart, LONG *plLength, 
    PAVISTREAM * ppResult); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

