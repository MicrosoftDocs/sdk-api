---
UID: NF:vfw.AVIStreamPrevKeyFrameTime
title: AVIStreamPrevKeyFrameTime macro
author: windows-sdk-content
description: The AVIStreamPrevKeyFrameTime macro returns the time of the previous key frame in the stream, starting at a given time.
old-location: multimedia\avistreamprevkeyframetime.htm
tech.root: Multimedia
ms.assetid: 0da49be2-b017-4d41-b9da-3c1310fa0289
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: AVIStreamPrevKeyFrameTime, AVIStreamPrevKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamPrevKeyFrameTime, multimedia.avistreamprevkeyframetime, vfw/AVIStreamPrevKeyFrameTime
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
 - AVIStreamPrevKeyFrameTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamPrevKeyFrameTime macro


## -description



The <b>AVIStreamPrevKeyFrameTime</b> macro returns the time of the previous key frame in the stream, starting at a given time.




## -parameters




### -param pavi

Handle to an open stream. 


### -param t

Position in the stream to begin searching. 


## -remarks



The search performed by this macro includes the frame that corresponds to the specified time.

The <b>AVIStreamPrevKeyFrameTime</b> macro is defined as follows:


```cpp

#define AVIStreamPrevKeyFrameTime(pavi, time) \ 
    AVIStreamSampleToTime(pavi, AVIStreamPrevKeyFrame(pavi, 
    AVIStreamTimeToSample(pavi, time))) 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

