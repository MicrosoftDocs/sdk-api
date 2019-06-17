---
UID: NF:vfw.AVIStreamLengthTime
title: AVIStreamLengthTime macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamLengthTime macro returns the length of a stream in time.
old-location: multimedia\avistreamlengthtime.htm
tech.root: Multimedia
ms.assetid: 550d04b2-d5d4-4acc-97d3-8cd180de1545
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamLengthTime, AVIStreamLengthTime macro [Windows Multimedia], _win32_AVIStreamLengthTime, multimedia.avistreamlengthtime, vfw/AVIStreamLengthTime
ms.topic: macro
f1_keywords: ["vfw/AVIStreamLengthTime"]
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
ms.custom: 19H1
---

# AVIStreamLengthTime macro


## -description



The <b>AVIStreamLengthTime</b> macro returns the length of a stream in time.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamLengthTime</b> macro is defined as follows:


```cpp

#define AVIStreamLengthTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamLength(pavi)) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

