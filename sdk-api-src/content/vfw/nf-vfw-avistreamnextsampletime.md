---
UID: NF:vfw.AVIStreamNextSampleTime
title: AVIStreamNextSampleTime macro
author: windows-sdk-content
description: The AVIStreamNextSampleTime macro returns the time that a sample changes to the next sample in the stream. This macro finds the next interesting time in a stream.
old-location: multimedia\avistreamnextsampletime.htm
tech.root: Multimedia
ms.assetid: 0421f082-9281-4cdb-8b33-2a90c14404dc
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: AVIStreamNextSampleTime, AVIStreamNextSampleTime macro [Windows Multimedia], _win32_AVIStreamNextSampleTime, multimedia.avistreamnextsampletime, vfw/AVIStreamNextSampleTime
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
 - AVIStreamNextSampleTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamNextSampleTime macro


## -description



The <b>AVIStreamNextSampleTime</b> macro returns the time that a sample changes to the next sample in the stream. This macro finds the next interesting time in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Position information of the sample in the stream. 


## -remarks



The <b>AVIStreamNextSampleTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamNextSampleTime(pavi, time) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamNextSample(pavi, \ 
    AVIStreamTimeToSample(pavi, t))) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

