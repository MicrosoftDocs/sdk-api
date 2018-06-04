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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Write(LONG lStart, LONG lSamples, LPVOID lpBuffer, 
    LONG cbBuffer, DWORD dwFlags, LONG *plSampWritten, 
    LONG *plBytesWritten); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

