---
UID: NF:vfw.AVIStreamIsKeyFrame
title: AVIStreamIsKeyFrame macro
author: windows-sdk-content
description: The AVIStreamIsKeyFrame macro indicates whether a sample in a specified stream is a key frame.
old-location: multimedia\avistreamiskeyframe.htm
tech.root: Multimedia
ms.assetid: 615ca0be-44d3-4dc4-9dc1-c14e8b50e835
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AVIStreamIsKeyFrame, AVIStreamIsKeyFrame macro [Windows Multimedia], _win32_AVIStreamIsKeyFrame, multimedia.avistreamiskeyframe, vfw/AVIStreamIsKeyFrame
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
 - AVIStreamIsKeyFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamIsKeyFrame macro


## -description



The <b>AVIStreamIsKeyFrame</b> macro indicates whether a sample in a specified stream is a key frame.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Position to search in the stream. 


## -remarks



The <b>AVIStreamIsKeyFrame</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamIsKeyFrame(pavi, lPos) \ 
    (AVIStreamNearestKeyFrame(pavi, lPos) == 1) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

