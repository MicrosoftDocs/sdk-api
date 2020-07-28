---
UID: NF:vfw.AVIStreamPrevSampleTime
title: AVIStreamPrevSampleTime macro (vfw.h)
description: The AVIStreamPrevSampleTime macro determines the time of the nearest nonempty sample that precedes a specified time in a stream.
helpviewer_keywords: ["AVIStreamPrevSampleTime","AVIStreamPrevSampleTime macro [Windows Multimedia]","_win32_AVIStreamPrevSampleTime","multimedia.avistreamprevsampletime","vfw/AVIStreamPrevSampleTime"]
old-location: multimedia\avistreamprevsampletime.htm
tech.root: Multimedia
ms.assetid: b116e33f-de51-4251-83be-96afceb99a69
ms.date: 12/05/2018
ms.keywords: AVIStreamPrevSampleTime, AVIStreamPrevSampleTime macro [Windows Multimedia], _win32_AVIStreamPrevSampleTime, multimedia.avistreamprevsampletime, vfw/AVIStreamPrevSampleTime
f1_keywords:
- vfw/AVIStreamPrevSampleTime
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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


```cpp

#define AVIStreamPrevSampleTime(pavi, time) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamPrevSample(pavi, \ 
    AVIStreamTimeToSample(pavi, t))) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

