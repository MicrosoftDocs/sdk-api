---
UID: NF:vfw.AVIStreamEndTime
title: AVIStreamEndTime macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamEndTime macro returns the time representing the end of the stream.
old-location: multimedia\avistreamendtime.htm
tech.root: Multimedia
ms.assetid: 0fd3c0c7-34cc-4193-8e6a-9866a9d651a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamEndTime, AVIStreamEndTime macro [Windows Multimedia], _win32_AVIStreamEndTime, multimedia.avistreamendtime, vfw/AVIStreamEndTime
ms.topic: macro
f1_keywords: 
 - "vfw/AVIStreamEndTime"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamEndTime macro


## -description



The <b>AVIStreamEndTime</b> macro returns the time representing the end of the stream.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamEndTime</b> macro is defined as follows:


```cpp

#define AVIStreamEndTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamEnd(pavi)) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

