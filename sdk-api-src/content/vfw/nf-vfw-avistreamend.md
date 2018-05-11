---
UID: NF:vfw.AVIStreamEnd
title: AVIStreamEnd macro
author: windows-driver-content
description: The AVIStreamEnd macro calculates the sample associated with the end of a stream.
old-location: multimedia\avistreamend.htm
old-project: Multimedia
ms.assetid: 9c132953-1b24-4a5f-b2e9-b5569a579696
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AVIStreamEnd, AVIStreamEnd macro [Windows Multimedia], _win32_AVIStreamEnd, multimedia.avistreamend, vfw/AVIStreamEnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	AVIStreamEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# AVIStreamEnd macro


## -description



The <b>AVIStreamEnd</b> macro calculates the sample associated with the end of a stream.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The sample number returned is not a valid sample number for reading data. It represents the end of the file. (The end of the file is equal to the start of the file plus its length.)

The <b>AVIStreamEnd</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamEnd(pavi) \ 
    (AVIStreamStart(pavi) + AVIStreamLength(pavi)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

