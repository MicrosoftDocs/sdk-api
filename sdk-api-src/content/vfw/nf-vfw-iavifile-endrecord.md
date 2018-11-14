---
UID: NF:vfw.IAVIFile.EndRecord
title: IAVIFile::EndRecord
author: windows-sdk-content
description: The EndRecord method writes the &#0034;REC&#0034; chunk in a tightly interleaved AVI file (having a one-to-one interleave factor of audio to video). Called when an application uses the AVIFileEndRecord function.
old-location: multimedia\iavifile_endrecord.htm
tech.root: Multimedia
ms.assetid: 43c4edbf-d736-4d85-9726-123f92145134
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: EndRecord, EndRecord method [Windows Multimedia], EndRecord method [Windows Multimedia],IAVIFile interface, IAVIFile interface [Windows Multimedia],EndRecord method, IAVIFile.EndRecord, IAVIFile::EndRecord, _win32_IAVIFile_EndRecord, multimedia.iavifile_endrecord, vfw/IAVIFile::EndRecord
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
 - IAVIFile.EndRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vfw.h
: 
- IAVIFile.EndRecord
: 
---

# IAVIFile::EndRecord


## -description



The <b>EndRecord</b> method writes the "REC" chunk in a tightly interleaved AVI file (having a one-to-one interleave factor of audio to video). Called when an application uses the <a href="https://msdn.microsoft.com/0f04c384-7702-43d4-9c7e-e9e74d6f2796">AVIFileEndRecord</a> function.




## -parameters






#### - pf

Pointer to the interface to a file.


## -returns



Returns the HRESULT defined by OLE.




## -remarks



This file handler method is typically not used.

For handlers written in C++, <b>EndRecord</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT EndRecord(VOID); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 

