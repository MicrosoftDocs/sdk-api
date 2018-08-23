---
UID: NF:vfw.IAVIStream.Info
title: IAVIStream::Info
author: windows-sdk-content
description: The Info method fills and returns an AVISTREAMINFO structure with information about a stream. Called when an application uses the AVIStreamInfo function.
old-location: multimedia\iavistream_info.htm
old-project: Multimedia
ms.assetid: c58c4d68-4d27-4c3c-a1f6-bdafa3633dae
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: IAVIStream interface [Windows Multimedia],Info method, IAVIStream.Info, IAVIStream::Info, Info, Info method [Windows Multimedia], Info method [Windows Multimedia],IAVIStream interface, _win32_IAVIStream_Info, multimedia.iavistream_info, vfw/IAVIStream::Info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vfw.h
req.include-header: 
req.redist: 
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
 - IAVIStream.Info
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IAVIStream::Info


## -description



The <b>Info</b> method fills and returns an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure with information about a stream. Called when an application uses the <a href="https://msdn.microsoft.com/7a1ba29b-e8ba-435d-a551-c9184631971c">AVIStreamInfo</a> function.




## -parameters




### -param psi

Pointer to an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure to contain stream information.


### -param lSize

Size, in bytes, of the structure specified by <i>psi</i>.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



If the buffer allocated is too small for the structure, the <b>Info</b> method should fail the call by returning AVIERR_BUFFERTOOSMALL. Otherwise, it should fill the structure and return its size.

For handlers written in C++, <b>Info</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT Info(AVIFILEINFO *psi, LONG lSize) 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

