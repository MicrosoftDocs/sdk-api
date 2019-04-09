---
UID: NF:strmif.IAMVideoCompression.put_WindowSize
title: IAMVideoCompression::put_WindowSize (strmif.h)
author: windows-sdk-content
description: The put_WindowSize method sets the number of frames over which the compressor must maintain an average data rate.
old-location: dshow\iamvideocompression_put_windowsize.htm
tech.root: DirectShow
ms.assetid: 744cd32d-5f61-4069-82c4-50bc1b800f24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMVideoCompression interface [DirectShow],put_WindowSize method, IAMVideoCompression.put_WindowSize, IAMVideoCompression::put_WindowSize, IAMVideoCompressionput_WindowSize, dshow.iamvideocompression_put_windowsize, put_WindowSize, put_WindowSize method [DirectShow], put_WindowSize method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_WindowSize
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression.put_WindowSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoCompression::put_WindowSize


## -description



The <code>put_WindowSize</code> method sets the number of frames over which the compressor must maintain an average data rate.



For example, assuming a data rate of 100K/sec and a frame rate of 10 frames per second, if the window size is 1, then every frame will be 10K or less. If the window size is 5, then every five consecutive frames must average 10K per frame, but individual frames may exceed this size.


## -parameters




### -param WindowSize [in]

Specifies the window size, expressed as a number of frames. .


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/1f12aa72-3468-4dca-a5f6-43f64f6d2f83">IAMVideoCompression::get_WindowSize</a>
 

 

