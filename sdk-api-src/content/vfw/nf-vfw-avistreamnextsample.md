---
UID: NF:vfw.AVIStreamNextSample
title: AVIStreamNextSample macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamNextSample macro locates the next nonempty sample from a specified position in a stream.
old-location: multimedia\avistreamnextsample.htm
tech.root: Multimedia
ms.assetid: 3ce1086f-4364-4d3c-a60e-7a82ecf8d708
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamNextSample, AVIStreamNextSample macro [Windows Multimedia], _win32_AVIStreamNextSample, multimedia.avistreamnextsample, vfw/AVIStreamNextSample
ms.topic: macro
f1_keywords: 
 - "vfw/AVIStreamNextSample"
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
 - AVIStreamNextSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamNextSample macro


## -description



The <b>AVIStreamNextSample</b> macro locates the next nonempty sample from a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The sample position returned does not include the sample specified by <i>lPos</i>.

The <b>AVIStreamNextSample</b> macro is defined as follows:


```cpp

#define AVIStreamNextSample(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos + 1, FIND_NEXT | FIND_ANY) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

