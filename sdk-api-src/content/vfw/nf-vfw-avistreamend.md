---
UID: NF:vfw.AVIStreamEnd
title: AVIStreamEnd macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamEnd macro calculates the sample associated with the end of a stream.
old-location: multimedia\avistreamend.htm
tech.root: Multimedia
ms.assetid: 9c132953-1b24-4a5f-b2e9-b5569a579696
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamEnd, AVIStreamEnd macro [Windows Multimedia], _win32_AVIStreamEnd, multimedia.avistreamend, vfw/AVIStreamEnd
ms.topic: macro
f1_keywords: 
 - "vfw/AVIStreamEnd"
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
 - AVIStreamEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamEnd macro


## -description



The <b>AVIStreamEnd</b> macro calculates the sample associated with the end of a stream.




## -parameters




### -param pavi

Handle to an open stream. 


## -remarks



The sample number returned is not a valid sample number for reading data. It represents the end of the file. (The end of the file is equal to the start of the file plus its length.)

The <b>AVIStreamEnd</b> macro is defined as follows:


```cpp

#define AVIStreamEnd(pavi) \ 
    (AVIStreamStart(pavi) + AVIStreamLength(pavi)) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

