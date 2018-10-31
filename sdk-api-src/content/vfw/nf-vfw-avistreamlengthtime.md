---
UID: NF:vfw.AVIStreamLengthTime
title: AVIStreamLengthTime macro
author: windows-sdk-content
description: The AVIStreamLengthTime macro returns the length of a stream in time.
old-location: multimedia\avistreamlengthtime.htm
tech.root: Multimedia
ms.assetid: 550d04b2-d5d4-4acc-97d3-8cd180de1545
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AVIStreamLengthTime, AVIStreamLengthTime macro [Windows Multimedia], _win32_AVIStreamLengthTime, multimedia.avistreamlengthtime, vfw/AVIStreamLengthTime
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
 - AVIStreamLengthTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamLengthTime macro


## -description



The <b>AVIStreamLengthTime</b> macro returns the length of a stream in time.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamLengthTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamLengthTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamLength(pavi)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

