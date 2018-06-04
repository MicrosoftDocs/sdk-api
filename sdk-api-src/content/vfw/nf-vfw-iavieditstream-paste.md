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

# IAVIEditStream::Paste


## -description



The <b>Paste</b> method copies a stream or a portion of it in another stream. Called when an application uses the <a href="https://msdn.microsoft.com/c3c77ec1-0aa4-47ab-afc1-ed69d6aca201">EditStreamPaste</a> function.




## -parameters




### -param plPos

Pointer to a buffer that receives the starting position of the operation.


### -param plLength

Pointer to a buffer that receives the length, in bytes, of the data to paste from the source stream.


### -param pstream

Pointer to the interface to the source stream.


### -param lStart

Starting position of the copy operation within the source stream.


### -param lEnd






#### - lLength

Length, in frames, of the copy operation within the source stream.


#### - pavi

Pointer to the interface to the stream to receive the pasted data.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Paste</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Paste(LONG *plPos, LONG *plLength, 
    PAVISTREAM pstream, LONG lStart, LONG lLength); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

