---
UID: NF:vfw.AVIStreamNearestSample
title: AVIStreamNearestSample macro
author: windows-sdk-content
description: The AVIStreamNearestSample macro locates the nearest nonempty sample at or preceding a specified position in a stream.
old-location: multimedia\avistreamnearestsample.htm
tech.root: Multimedia
ms.assetid: 350255b7-35ae-4eed-8991-82b548a2fa65
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AVIStreamNearestSample, AVIStreamNearestSample macro [Windows Multimedia], _win32_AVIStreamNearestSample, multimedia.avistreamnearestsample, vfw/AVIStreamNearestSample
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
 - AVIStreamNearestSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- AVIStreamNearestSample
: 
---

# AVIStreamNearestSample macro


## -description



The <b>AVIStreamNearestSample</b> macro locates the nearest nonempty sample at or preceding a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The <b>AVIStreamNearestSample</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNearestSample(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos, FIND_PREV | FIND_ANY) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

