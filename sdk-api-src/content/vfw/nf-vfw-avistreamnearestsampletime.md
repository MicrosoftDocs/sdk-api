---
UID: NF:vfw.AVIStreamNearestSampleTime
title: AVIStreamNearestSampleTime macro (vfw.h)
description: The AVIStreamNearestSampleTime macro determines the time corresponding to the beginning of a sample that is nearest to a specified time in a stream.helpviewer_keywords: ["AVIStreamNearestSampleTime","AVIStreamNearestSampleTime macro [Windows Multimedia]","_win32_AVIStreamNearestSampleTime","multimedia.avistreamnearestsampletime","vfw/AVIStreamNearestSampleTime"]
old-location: multimedia\avistreamnearestsampletime.htm
tech.root: Multimedia
ms.assetid: 8f9bd7b8-24b4-4bc5-98f0-0339bbaa0caf
ms.date: 12/05/2018
ms.keywords: AVIStreamNearestSampleTime, AVIStreamNearestSampleTime macro [Windows Multimedia], _win32_AVIStreamNearestSampleTime, multimedia.avistreamnearestsampletime, vfw/AVIStreamNearestSampleTime
f1_keywords:
- vfw/AVIStreamNearestSampleTime
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
- AVIStreamNearestSampleTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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


```cpp

#define AVIStreamNearestSampleTime(pavi, lTime) \ 
    AVIStreamSampleToTime(pavi, AVIStreamNearestSample(pavi, 
    AVIStreamTimeToSample(pavi, lTime))) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

