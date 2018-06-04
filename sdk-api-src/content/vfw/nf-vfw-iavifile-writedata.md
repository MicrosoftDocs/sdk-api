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

# IAVIFile::WriteData


## -description



The <b>WriteData</b> method writes file headers. Called when an application uses the <a href="https://msdn.microsoft.com/27eef026-e401-44a2-9b46-a16b61026d2a">AVIFileWriteData</a> function.




## -parameters




### -param ckid




### -param lpData




### -param cbData






#### - cbBuffer

Size, in bytes, of the buffer specified by <i>lpBuffer</i>.


#### - fcc

Four-character code of the header to write.


#### - lpBuffer

Pointer to the buffer for the data.


#### - ps

Pointer to the interface to a file.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>WriteData</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT WriteData(DWORD fcc, LPVOID lpBuffer, LONG cbBuffer); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

