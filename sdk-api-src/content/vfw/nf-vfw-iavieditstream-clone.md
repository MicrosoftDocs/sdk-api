---
UID: NF:vfw.IAVIEditStream.Clone
title: IAVIEditStream::Clone
author: windows-sdk-content
description: The Clone method duplicates a stream. Called when an application uses the EditStreamClone function.
old-location: multimedia\iavieditstream_clone.htm
old-project: Multimedia
ms.assetid: 7112056e-5e25-4262-abe3-5cbb0675a475
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: Clone, Clone method [Windows Multimedia], Clone method [Windows Multimedia],IAVIEditStream interface, IAVIEditStream interface [Windows Multimedia],Clone method, IAVIEditStream.Clone, IAVIEditStream::Clone, _win32_IAVIEditStream_Clone, multimedia.iavieditstream_clone, vfw/IAVIEditStream::Clone
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIEditStream.Clone
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIEditStream::Clone


## -description



The <b>Clone</b> method duplicates a stream. Called when an application uses the <a href="https://msdn.microsoft.com/2a512dbd-8d17-43d0-a074-571b4c1837c7">EditStreamClone</a> function.




## -parameters




### -param ppResult

Pointer to a buffer that receives a pointer to the interface to the new stream.


#### - pavi

Pointer to the interface to the stream being cloned.


## -returns



The method returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>Clone</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Clone(PAVISTREAM *ppResult); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

