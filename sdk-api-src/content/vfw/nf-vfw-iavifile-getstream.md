---
UID: NF:vfw.IAVIFile.GetStream
title: IAVIFile::GetStream
author: windows-sdk-content
description: The GetStream method opens a stream by accessing it in a file. Called when an application uses the AVIFileGetStream function.
old-location: multimedia\iavifile_getstream.htm
tech.root: Multimedia
ms.assetid: 66ab2d8f-39f5-4eec-a873-c6f554e3b8ff
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetStream, GetStream method [Windows Multimedia], GetStream method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],GetStream method, IAVIFile.GetStream, IAVIFile::GetStream, _win32_IAVIFile_GetStream, multimedia.iavifile_getstream, vfw/IAVIFile::GetStream
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
 - IAVIFile.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

