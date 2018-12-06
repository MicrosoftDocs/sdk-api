---
UID: NF:vfw.AVIStreamSampleSize
title: AVIStreamSampleSize macro
author: windows-sdk-content
description: The AVIStreamRelease macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by lPos.
old-location: multimedia\avistreamsamplesize.htm
tech.root: Multimedia
ms.assetid: 24d8dae6-a9f7-4ca6-a083-1e1f59c0591c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AVIStreamSampleSize, AVIStreamSampleSize macro [Windows Multimedia], _win32_AVIStreamSampleSize, multimedia.avistreamsamplesize, vfw/AVIStreamSampleSize
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
 - AVIStreamSampleSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamSampleSize macro


## -description



The <a href="https://msdn.microsoft.com/bd71ddf6-9d02-463d-9d1c-50605441ad59">AVIStreamRelease</a> macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by <i>lPos</i>.




## -parameters




### -param pavi

Handle to an open stream. 


### -param lPos

Position of a sample in the stream. 


### -param plSize

Address to contain the buffer size. 


## -remarks



The <b>AVIStreamSampleSize</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamSampleSize(pavi, lPos, plSize) \ 
    AVIStreamRead(pavi, lPos, 1, NULL, 0, plSize, NULL) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

