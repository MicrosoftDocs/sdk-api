---
UID: NF:vfw.AVIStreamNextKeyFrame
title: AVIStreamNextKeyFrame macro (vfw.h)
description: The AVIStreamNextKeyFrame macro locates the next key frame following a specified position in a stream.
helpviewer_keywords: ["AVIStreamNextKeyFrame","AVIStreamNextKeyFrame macro [Windows Multimedia]","_win32_AVIStreamNextKeyFrame","multimedia.avistreamnextkeyframe","vfw/AVIStreamNextKeyFrame"]
old-location: multimedia\avistreamnextkeyframe.htm
tech.root: Multimedia
ms.assetid: 928b5deb-2f68-4fed-98cf-8130379c8622
ms.date: 12/05/2018
ms.keywords: AVIStreamNextKeyFrame, AVIStreamNextKeyFrame macro [Windows Multimedia], _win32_AVIStreamNextKeyFrame, multimedia.avistreamnextkeyframe, vfw/AVIStreamNextKeyFrame
f1_keywords:
- vfw/AVIStreamNextKeyFrame
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
- AVIStreamNextKeyFrame
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamNextKeyFrame macro


## -description



The <b>AVIStreamNextKeyFrame</b> macro locates the next key frame following a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The search performed by this macro does not include the frame at the specified position.

The <b>AVIStreamNextKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamNextKeyFrame(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos + 1, FIND_NEXT | FIND_KEY) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

