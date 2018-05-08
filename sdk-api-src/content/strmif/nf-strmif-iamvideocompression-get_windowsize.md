---
UID: NF:strmif.IAMVideoCompression.get_WindowSize
title: IAMVideoCompression::get_WindowSize
author: windows-driver-content
description: The get_WindowSize method retrieves the number of frames over which the compressor will maintain the average data rate.
old-location: dshow\iamvideocompression_get_windowsize.htm
old-project: DirectShow
ms.assetid: 1f12aa72-3468-4dca-a5f6-43f64f6d2f83
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMVideoCompression interface [DirectShow],get_WindowSize method, IAMVideoCompression.get_WindowSize, IAMVideoCompression::get_WindowSize, IAMVideoCompressionget_WindowSize, dshow.iamvideocompression_get_windowsize, get_WindowSize, get_WindowSize method [DirectShow], get_WindowSize method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_WindowSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVideoCompression.get_WindowSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoCompression::get_WindowSize


## -description



The <code>get_WindowSize</code> method retrieves the number of frames over which the compressor will maintain the average data rate.



For example, assuming a data rate of 100K/sec and a frame rate of 10 frames per second, if the window size is 1, then every frame will be 10K or less. If the window size is 5, then every five consecutive frames will average 10K per frame, but individual frames may exceed this size.

The default window size is 1.


## -parameters




### -param pWindowSize [out]

Pointer to a variable that receives the window size, expressed as a number of frames.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/744cd32d-5f61-4069-82c4-50bc1b800f24">IAMVideoCompression::put_WindowSize</a>
 

 

