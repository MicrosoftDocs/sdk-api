---
UID: NF:vfw.AVIStreamNextSample
title: AVIStreamNextSample macro
author: windows-sdk-content
description: The AVIStreamNextSample macro locates the next nonempty sample from a specified position in a stream.
old-location: multimedia\avistreamnextsample.htm
tech.root: Multimedia
ms.assetid: 3ce1086f-4364-4d3c-a60e-7a82ecf8d708
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AVIStreamNextSample, AVIStreamNextSample macro [Windows Multimedia], _win32_AVIStreamNextSample, multimedia.avistreamnextsample, vfw/AVIStreamNextSample
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIStreamNextSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamNextSample macro


## -description



The <b>AVIStreamNextSample</b> macro locates the next nonempty sample from a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The sample position returned does not include the sample specified by <i>lPos</i>.

The <b>AVIStreamNextSample</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNextSample(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos + 1, FIND_NEXT | FIND_ANY) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

