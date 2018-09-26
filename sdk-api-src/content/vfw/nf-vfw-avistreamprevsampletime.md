---
UID: NF:vfw.AVIStreamPrevSampleTime
title: AVIStreamPrevSampleTime macro
author: windows-sdk-content
description: The AVIStreamPrevSampleTime macro determines the time of the nearest nonempty sample that precedes a specified time in a stream.
old-location: multimedia\avistreamprevsampletime.htm
tech.root: Multimedia
ms.assetid: b116e33f-de51-4251-83be-96afceb99a69
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: AVIStreamPrevSampleTime, AVIStreamPrevSampleTime macro [Windows Multimedia], _win32_AVIStreamPrevSampleTime, multimedia.avistreamprevsampletime, vfw/AVIStreamPrevSampleTime
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
 - AVIStreamPrevSampleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamPrevSampleTime macro


## -description



The <b>AVIStreamPrevSampleTime</b> macro determines the time of the nearest nonempty sample that precedes a specified time in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Position information of the sample in the stream. 


## -remarks



The <b>AVIStreamPrevSampleTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamPrevSampleTime(pavi, time) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamPrevSample(pavi, \ 
    AVIStreamTimeToSample(pavi, t))) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

