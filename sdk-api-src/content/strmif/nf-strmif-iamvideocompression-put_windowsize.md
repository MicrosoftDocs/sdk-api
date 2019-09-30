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
f1_keywords: 
 - "strmif/IAMVideoCompression.put_WindowSize"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamvideocompression-get_windowsize">IAMVideoCompression::get_WindowSize</a>
 

 

