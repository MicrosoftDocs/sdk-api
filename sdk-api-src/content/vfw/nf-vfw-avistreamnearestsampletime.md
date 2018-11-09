---
UID: NF:vfw.AVIStreamNearestSampleTime
title: AVIStreamNearestSampleTime macro
author: windows-sdk-content
description: The AVIStreamNearestSampleTime macro determines the time corresponding to the beginning of a sample that is nearest to a specified time in a stream.
old-location: multimedia\avistreamnearestsampletime.htm
tech.root: Multimedia
ms.assetid: 8f9bd7b8-24b4-4bc5-98f0-0339bbaa0caf
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: AVIStreamNearestSampleTime, AVIStreamNearestSampleTime macro [Windows Multimedia], _win32_AVIStreamNearestSampleTime, multimedia.avistreamnearestsampletime, vfw/AVIStreamNearestSampleTime
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
 - AVIStreamNearestSampleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamNearestSampleTime macro


## -description



The <b>AVIStreamNearestSampleTime</b> macro determines the time corresponding to the beginning of a sample that is nearest to a specified time in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Starting time, in milliseconds, to search in the stream. 


## -remarks



The <b>AVIStreamNearestSampleTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNearestSampleTime(pavi, lTime) \ 
    AVIStreamSampleToTime(pavi, AVIStreamNearestSample(pavi, 
    AVIStreamTimeToSample(pavi, lTime))) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

