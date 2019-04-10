---
UID: NF:vfw.AVIStreamNextKeyFrameTime
title: AVIStreamNextKeyFrameTime macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamNextKeyFrameTime macro returns the time of the next key frame in the stream, starting at a given time.
old-location: multimedia\avistreamnextkeyframetime.htm
tech.root: Multimedia
ms.assetid: 5eb338aa-6ccb-4adc-a46c-9f796c36a121
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamNextKeyFrameTime, AVIStreamNextKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamNextKeyFrameTime, multimedia.avistreamnextkeyframetime, vfw/AVIStreamNextKeyFrameTime
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
 - AVIStreamNextKeyFrameTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamNextKeyFrameTime macro


## -description



The <b>AVIStreamNextKeyFrameTime</b> macro returns the time of the next key frame in the stream, starting at a given time.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Position in the stream to begin searching. 


## -remarks



The search performed by this macro includes the frame that corresponds to the specified time.

The <b>AVIStreamNextKeyFrameTime</b> macro is defined as follows:


```cpp

#define AVIStreamNextKeyFrameTime(pavi, time) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamNextKeyFrame(pavi, \ 
    AVIStreamTimeToSample(pavi, time))) 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

