---
UID: NF:vfw.IAVIEditStream.SetInfo
title: IAVIEditStream::SetInfo
author: windows-sdk-content
description: The SetInfo method changes the characteristics of a stream. Called when an application uses the EditStreamSetInfo function.
old-location: multimedia\iavieditstream_setinfo.htm
tech.root: Multimedia
ms.assetid: 46496c24-cbe0-4234-8683-f39fa58e076b
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: IAVIEditStream interface [Windows Multimedia],SetInfo method, IAVIEditStream.SetInfo, IAVIEditStream::SetInfo, SetInfo, SetInfo method [Windows Multimedia], SetInfo method [Windows Multimedia],IAVIEditStream interface, _win32_IAVIEditStream_SetInfo, multimedia.iavieditstream_setinfo, vfw/IAVIEditStream::SetInfo
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
 - IAVIEditStream.SetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAVIEditStream::SetInfo


## -description



The <b>SetInfo</b> method changes the characteristics of a stream. Called when an application uses the <a href="https://msdn.microsoft.com/c9b33a91-b7b1-4b66-86ba-d1ea774c8743">EditStreamSetInfo</a> function.




## -parameters




### -param lpInfo

Pointer to an <a href="https://msdn.microsoft.com/dca6d9ca-a825-4bd0-a19d-0655d775fdfb">AVISTREAMINFO</a> structure containing the new stream characteristics.


### -param cbInfo

Size, in bytes, of the buffer.


#### - pavi

Pointer to the interface to a stream.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



For handlers written in C++, <b>SetInfo</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT SetInfo(AVISTREAMINFO *lpInfo, LONG cbInfo); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>



<a href="https://msdn.microsoft.com/c9b33a91-b7b1-4b66-86ba-d1ea774c8743">EditStreamSetInfo</a>
 

 

