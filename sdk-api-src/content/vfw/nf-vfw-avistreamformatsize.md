---
UID: NF:vfw.AVIStreamFormatSize
title: AVIStreamFormatSize macro
author: windows-sdk-content
description: The AVIStreamFormatSize macro determines the buffer size, in bytes, needed to store format information for a sample in a stream.
old-location: multimedia\avistreamformatsize.htm
tech.root: Multimedia
ms.assetid: e29bbbc3-28b2-44d3-b1f1-66ad2b29a7a3
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: AVIStreamFormatSize, AVIStreamFormatSize macro [Windows Multimedia], _win32_AVIStreamFormatSize, multimedia.avistreamformatsize, vfw/AVIStreamFormatSize
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
 - AVIStreamFormatSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AVIStreamFormatSize macro


## -description



The <b>AVIStreamFormatSize</b> macro determines the buffer size, in bytes, needed to store format information for a sample in a stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param lPos

Position of a sample in the stream. 


### -param plSize

Address to contain the buffer size. 


## -remarks



The <b>AVIStreamFormatSize</b> macro is defined as follows:


```cpp

#define AVIStreamFormatSize(pavi, lPos, plSize) \ 
    AVIStreamReadFormat(pavi, lPos, NULL, plSize) 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

