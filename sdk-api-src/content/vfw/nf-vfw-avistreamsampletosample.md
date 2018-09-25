---
UID: NF:vfw.AVIStreamSampleToSample
title: AVIStreamSampleToSample macro
author: windows-sdk-content
description: The AVIStreamSampleToSample macro returns the sample in a stream that occurs at the same time as a sample that occurs in a second stream.
old-location: multimedia\avistreamsampletosample.htm
tech.root: Multimedia
ms.assetid: ed726651-d8f3-4dba-b81d-e283733cabe2
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AVIStreamSampleToSample, AVIStreamSampleToSample macro [Windows Multimedia], _win32_AVIStreamSampleToSample, multimedia.avistreamsampletosample, vfw/AVIStreamSampleToSample
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
 - AVIStreamSampleToSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamSampleToSample macro


## -description



The <b>AVIStreamSampleToSample</b> macro returns the sample in a stream that occurs at the same time as a sample that occurs in a second stream.




## -parameters




### -param pavi1

Handle to an open stream that contains the sample that is returned. 


### -param pavi2

Handle to a second stream that contains the reference sample. 


### -param l

Position information of the sample in the stream referenced by pavi2. 


## -remarks



The <b>AVIStreamSampleToSample</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define AVIStreamSampleToSample(pavi1, pavi2, lsample) \ 
    AVIStreamTimeToSample(pavi1, AVIStreamSampleToTime \ 
    (pavi2, lsample)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

