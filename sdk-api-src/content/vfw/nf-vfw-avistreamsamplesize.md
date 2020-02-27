---
UID: NF:vfw.AVIStreamSampleSize
title: AVIStreamSampleSize macro (vfw.h)
description: The AVIStreamRelease macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by lPos.
old-location: multimedia\avistreamsamplesize.htm
tech.root: Multimedia
ms.assetid: 24d8dae6-a9f7-4ca6-a083-1e1f59c0591c
ms.date: 12/05/2018
ms.keywords: AVIStreamSampleSize, AVIStreamSampleSize macro [Windows Multimedia], _win32_AVIStreamSampleSize, multimedia.avistreamsamplesize, vfw/AVIStreamSampleSize
f1_keywords:
- vfw/AVIStreamSampleSize
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
- AVIStreamSampleSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamSampleSize macro


## -description



The <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-avistreamrelease">AVIStreamRelease</a> macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by <i>lPos</i>.




## -parameters




### -param pavi

Handle to an open stream. 


### -param lPos

Position of a sample in the stream. 


### -param plSize

Address to contain the buffer size. 


## -remarks



The <b>AVIStreamSampleSize</b> macro is defined as follows:


```cpp

#define AVIStreamSampleSize(pavi, lPos, plSize) \ 
    AVIStreamRead(pavi, lPos, 1, NULL, 0, plSize, NULL) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

