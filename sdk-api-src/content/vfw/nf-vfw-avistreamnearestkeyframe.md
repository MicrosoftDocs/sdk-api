---
UID: NF:vfw.AVIStreamNearestKeyFrame
title: AVIStreamNearestKeyFrame macro (vfw.h)
description: The AVIStreamNearestKeyFrame macro locates the key frame at or preceding a specified position in a stream.
helpviewer_keywords: ["AVIStreamNearestKeyFrame","AVIStreamNearestKeyFrame macro [Windows Multimedia]","_win32_AVIStreamNearestKeyFrame","multimedia.avistreamnearestkeyframe","vfw/AVIStreamNearestKeyFrame"]
old-location: multimedia\avistreamnearestkeyframe.htm
tech.root: Multimedia
ms.assetid: 90d0e0a8-dc5b-4f7e-868e-03f40f037437
ms.date: 12/05/2018
ms.keywords: AVIStreamNearestKeyFrame, AVIStreamNearestKeyFrame macro [Windows Multimedia], _win32_AVIStreamNearestKeyFrame, multimedia.avistreamnearestkeyframe, vfw/AVIStreamNearestKeyFrame
f1_keywords:
- vfw/AVIStreamNearestKeyFrame
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
- AVIStreamNearestKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamNearestKeyFrame macro


## -description



The <b>AVIStreamNearestKeyFrame</b> macro locates the key frame at or preceding a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The <b>AVIStreamNearestKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamNearestKeyFrame(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos , FIND_PREV | FIND_KEY) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

