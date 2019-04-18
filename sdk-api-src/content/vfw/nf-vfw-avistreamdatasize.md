---
UID: NF:vfw.AVIStreamDataSize
title: AVIStreamDataSize macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamDataSize macro determines the buffer size, in bytes, needed to retrieve optional header data for a specified stream.
old-location: multimedia\avistreamdatasize.htm
tech.root: Multimedia
ms.assetid: e91258ee-b90a-43b9-9d5e-0adee215714c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamDataSize, AVIStreamDataSize macro [Windows Multimedia], _win32_AVIStreamDataSize, multimedia.avistreamdatasize, vfw/AVIStreamDataSize
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
 - AVIStreamDataSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamDataSize macro


## -description



The <b>AVIStreamDataSize</b> macro determines the buffer size, in bytes, needed to retrieve optional header data for a specified stream.




## -parameters




### -param pavi

Handle to an open stream. 


### -param fcc

Four-character code specifying the stream type. 


### -param plSize

Address to contain the buffer size for the optional header data. 


## -remarks



The <b>AVIStreamDataSize</b> macro is defined as follows:


```cpp

#define AVIStreamDataSize(pavi, fcc, plSize) \ 
    AVIStreamReadData(pavi, fcc, NULL, plSize) 
 

```





## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/5544e706-89e9-46e8-8703-ad978e675bbf">AVIFile Macros</a>
 

 

