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

# IAVIFile::GetStream


## -description



The <b>GetStream</b> method opens a stream by accessing it in a file. Called when an application uses the <a href="https://msdn.microsoft.com/b51a823c-6904-4942-883f-bda347541757">AVIFileGetStream</a> function.




## -parameters




### -param ppStream

Pointer to a buffer that receives a pointer to the interface to a stream.


### -param fccType

Four-character code indicating the type of stream to locate.


### -param lParam

Stream number.


#### - pf

Pointer to the interface to a file.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



It is typically easier to implement this method by creating all of the stream objects in advance by using the <a href="https://msdn.microsoft.com/4a0c0154-ea38-471d-94c3-799a6ba47c2f">IAVIFile::Open</a> method. Then, this method accesses the interface to the specified stream.

Remember to increment the reference count maintained by the <b>AddRef</b> method for the stream when this method is used.

For handlers written in C++, GetStream has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT GetStream(PAVISTREAM *ppStream, 
    DWORD fccType, LONG lParam); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

