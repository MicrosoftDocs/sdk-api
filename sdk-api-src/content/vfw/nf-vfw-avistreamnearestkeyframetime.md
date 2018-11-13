---
UID: NF:vfw.AVIStreamNearestKeyFrameTime
title: AVIStreamNearestKeyFrameTime macro
author: windows-sdk-content
description: The AVIStreamNearestKeyFrameTime macro determines the time corresponding to the beginning of the key frame nearest (at or preceding) a specified time in a stream.
old-location: multimedia\avistreamnearestkeyframetime.htm
tech.root: Multimedia
ms.assetid: 7409e8e3-d151-4970-9c0e-84ecdf9846a0
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AVIStreamNearestKeyFrameTime, AVIStreamNearestKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamNearestKeyFrameTime, multimedia.avistreamnearestkeyframetime, vfw/AVIStreamNearestKeyFrameTime
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
 - AVIStreamNearestKeyFrameTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamNearestKeyFrameTime macro


## -description



The <b>AVIStreamNearestKeyFrameTime</b> macro determines the time corresponding to the beginning of the key frame nearest (at or preceding) a specified time in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Starting time, in milliseconds, to search in the stream. 


## -remarks



The <b>AVIStreamNearestKeyFrameTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNearestKeyFrameTime(pavi, lTime) \ 
    AVIStreamSampleToTime(pavi, AVIStreamNearestKeyFrame(pavi, 
    AVIStreamTimeToSample(pavi, lTime))) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

