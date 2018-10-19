---
UID: NF:vfw.AVIStreamStartTime
title: AVIStreamStartTime macro
author: windows-sdk-content
description: The AVIStreamStartTime macro returns the starting time of a stream's first sample.
old-location: multimedia\avistreamstarttime.htm
tech.root: Multimedia
ms.assetid: 6bfa053f-26ca-4dc8-8896-11ee9f0d9b77
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AVIStreamStartTime, AVIStreamStartTime macro [Windows Multimedia], _win32_AVIStreamStartTime, multimedia.avistreamstarttime, vfw/AVIStreamStartTime
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
 - AVIStreamStartTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamStartTime macro


## -description



The <b>AVIStreamStartTime</b> macro returns the starting time of a stream's first sample.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The <b>AVIStreamStartTime</b> macro is defined as follows:


```cpp

#define AVIStreamStartTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamStart(pavi)) 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

