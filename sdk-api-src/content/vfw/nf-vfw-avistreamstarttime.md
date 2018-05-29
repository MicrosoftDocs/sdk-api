---
UID: NF:vfw.AVIStreamStartTime
title: AVIStreamStartTime macro
author: windows-sdk-content
description: The AVIStreamStartTime macro returns the starting time of a stream's first sample.
old-location: multimedia\avistreamstarttime.htm
old-project: Multimedia
ms.assetid: 6bfa053f-26ca-4dc8-8896-11ee9f0d9b77
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: AVIStreamStartTime, AVIStreamStartTime macro [Windows Multimedia], _win32_AVIStreamStartTime, multimedia.avistreamstarttime, vfw/AVIStreamStartTime
ms.prod: windows
ms.technology: windows-sdk
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
-	AVIStreamStartTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# AVIStreamStartTime macro


## -description



The <b>AVIStreamStartTime</b> macro returns the starting time of a stream's first sample.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamStartTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamStartTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamStart(pavi)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

