---
UID: NF:vfw.AVIStreamPrevKeyFrame
title: AVIStreamPrevKeyFrame macro
author: windows-sdk-content
description: The AVIStreamPrevKeyFrame macro locates the key frame that precedes a specified position in a stream.
old-location: multimedia\avistreamprevkeyframe.htm
tech.root: Multimedia
ms.assetid: 69933c8f-7e4e-45b2-aa72-ac127f3c8d05
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AVIStreamPrevKeyFrame, AVIStreamPrevKeyFrame macro [Windows Multimedia], _win32_AVIStreamPrevKeyFrame, multimedia.avistreamprevkeyframe, vfw/AVIStreamPrevKeyFrame
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
 - AVIStreamPrevKeyFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamPrevKeyFrame macro


## -description



The <b>AVIStreamPrevKeyFrame</b> macro locates the key frame that precedes a specified position in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param l

Starting position to search in the stream. 


## -remarks



The search performed by this macro does not include the frame at the specified position.

The <b>AVIStreamPrevKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamPrevKeyFrame(pavi, lPos) \ 
    AVIStreamFindSample(pavi, lPos - 1, FIND_PREV | FIND_KEY) 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

