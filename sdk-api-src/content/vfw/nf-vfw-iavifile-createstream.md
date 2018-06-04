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

# IAVIFile::CreateStream


## -description



The <b>CreateStream</b> method creates a stream for writing. Called when an application uses the <a href="https://msdn.microsoft.com/bff87fbb-fcd8-4dd4-93d0-9cab39c30409">AVIFileCreateStream</a> function.




## -parameters




### -param ppStream




### -param psi

Pointer to an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure defining the stream to create.


#### - pf

Pointer to the interface to a file.


#### - ppstream

Pointer to a buffer that receives a pointer to the interface to the new stream.


## -returns



Returns HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>CreateStream</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT CreateStream(PAVISTREAM *ppstream, 
    AVISTREAMINFO *psi); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

