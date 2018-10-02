---
UID: NF:vfw.AVIStreamEndTime
title: AVIStreamEndTime macro
author: windows-sdk-content
description: The AVIStreamEndTime macro returns the time representing the end of the stream.
old-location: multimedia\avistreamendtime.htm
tech.root: Multimedia
ms.assetid: 0fd3c0c7-34cc-4193-8e6a-9866a9d651a2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AVIStreamEndTime, AVIStreamEndTime macro [Windows Multimedia], _win32_AVIStreamEndTime, multimedia.avistreamendtime, vfw/AVIStreamEndTime
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
 - AVIStreamEndTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamEndTime macro


## -description



The <b>AVIStreamEndTime</b> macro returns the time representing the end of the stream.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamEndTime</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamEndTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamEnd(pavi)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

