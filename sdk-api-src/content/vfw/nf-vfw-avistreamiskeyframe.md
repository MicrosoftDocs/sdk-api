---
UID: NF:vfw.AVIStreamIsKeyFrame
title: AVIStreamIsKeyFrame macro (vfw.h)
description: The AVIStreamIsKeyFrame macro indicates whether a sample in a specified stream is a key frame.helpviewer_keywords: ["AVIStreamIsKeyFrame","AVIStreamIsKeyFrame macro [Windows Multimedia]","_win32_AVIStreamIsKeyFrame","multimedia.avistreamiskeyframe","vfw/AVIStreamIsKeyFrame"]
old-location: multimedia\avistreamiskeyframe.htm
tech.root: Multimedia
ms.assetid: 615ca0be-44d3-4dc4-9dc1-c14e8b50e835
ms.date: 12/05/2018
ms.keywords: AVIStreamIsKeyFrame, AVIStreamIsKeyFrame macro [Windows Multimedia], _win32_AVIStreamIsKeyFrame, multimedia.avistreamiskeyframe, vfw/AVIStreamIsKeyFrame
f1_keywords:
- vfw/AVIStreamIsKeyFrame
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
- AVIStreamIsKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamIsKeyFrame macro


## -description



The <b>AVIStreamIsKeyFrame</b> macro indicates whether a sample in a specified stream is a key frame.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Position to search in the stream. 


## -remarks



The <b>AVIStreamIsKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamIsKeyFrame(pavi, lPos) \ 
    (AVIStreamNearestKeyFrame(pavi, lPos) == 1) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

