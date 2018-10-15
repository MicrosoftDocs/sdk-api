---
UID: NF:vfw.AVIStreamNextKeyFrame
title: AVIStreamNextKeyFrame macro
author: windows-sdk-content
description: The AVIStreamNextKeyFrame macro locates the next key frame following a specified position in a stream.
old-location: multimedia\avistreamnextkeyframe.htm
tech.root: Multimedia
ms.assetid: 928b5deb-2f68-4fed-98cf-8130379c8622
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AVIStreamNextKeyFrame, AVIStreamNextKeyFrame macro [Windows Multimedia], _win32_AVIStreamNextKeyFrame, multimedia.avistreamnextkeyframe, vfw/AVIStreamNextKeyFrame
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
 - AVIStreamNextKeyFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

