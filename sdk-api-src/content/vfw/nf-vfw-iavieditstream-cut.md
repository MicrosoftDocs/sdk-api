---
UID: NF:vfw.IAVIEditStream.Cut
title: IAVIEditStream::Cut
author: windows-sdk-content
description: The Cut method removes a portion of a stream and places it in a temporary stream. Called when an application uses the EditStreamCut function.
old-location: multimedia\iavieditstream_cut.htm
tech.root: Multimedia
ms.assetid: e889d435-5c33-402d-bd69-c9122670e404
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Cut, Cut method [Windows Multimedia], Cut method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Cut method, IAVIEditStream.Cut, IAVIEditStream::Cut, _win32_IAVIEditStream_Cut, multimedia.iavieditstream_cut, vfw/IAVIEditStream::Cut
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
 - IAVIEditStream.Cut
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIEditStream::Cut


## -description



The <b>Cut</b> method removes a portion of a stream and places it in a temporary stream. Called when an application uses the <a href="https://msdn.microsoft.com/201f977c-926b-470c-b1ae-62946e6f691e">EditStreamCut</a> function.




## -parameters




### -param plStart

Pointer to a buffer that receives the starting position of the operation.


### -param plLength

Pointer to a buffer that receives the length, in frames, of the operation.


### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream to cut.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Cut</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Cut(LONG *plStart, LONG *plLength, 
    PAVISTREAM *ppResult); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

