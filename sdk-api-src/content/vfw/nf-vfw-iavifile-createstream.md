---
UID: NF:vfw.IAVIFile.CreateStream
title: IAVIFile::CreateStream
author: windows-driver-content
description: The CreateStream method creates a stream for writing. Called when an application uses the AVIFileCreateStream function.
old-location: multimedia\iavifile_createstream.htm
old-project: Multimedia
ms.assetid: 5c922bb0-53ca-4285-861a-4701503b0445
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CreateStream, CreateStream method [Windows Multimedia], CreateStream method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],CreateStream method, IAVIFile.CreateStream, IAVIFile::CreateStream, _win32_IAVIFile_CreateStream, multimedia.iavifile_createstream, vfw/IAVIFile::CreateStream
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IAVIFile.CreateStream
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 

