---
UID: NF:vfw.IAVIStream.Delete
title: IAVIStream::Delete
author: windows-sdk-content
description: The Delete method deletes data from a stream.
old-location: multimedia\iavistream_delete.htm
tech.root: Multimedia
ms.assetid: 0872023e-a760-4080-99da-df2941b84611
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Delete, Delete method [Windows Multimedia], Delete method [Windows Multimedia],IAVIStream interface, IAVIStream interface [Windows Multimedia],Delete method, IAVIStream.Delete, IAVIStream::Delete, _win32_IAVIStream_Delete, multimedia.iavistream_delete, vfw/IAVIStream::Delete
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
 - IAVIStream.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIStream::Delete


## -description



The <b>Delete</b> method deletes data from a stream.




## -parameters




### -param lStart

Starting sample or frame number to delete.


### -param lSamples

Number of samples to delete.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Delete</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Delete(LONG lStart, LONG lSamples); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

