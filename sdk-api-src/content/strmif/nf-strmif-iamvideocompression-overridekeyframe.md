---
UID: NF:strmif.IAMVideoCompression.OverrideKeyFrame
title: IAMVideoCompression::OverrideKeyFrame
author: windows-sdk-content
description: The OverrideKeyFrame method instructs the filter to compress a particular frame as a key frame.
old-location: dshow\iamvideocompression_overridekeyframe.htm
tech.root: DirectShow
ms.assetid: 2e8e52b9-cc66-42f5-a0ea-110188bfcf8b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAMVideoCompression interface [DirectShow],OverrideKeyFrame method, IAMVideoCompression.OverrideKeyFrame, IAMVideoCompression::OverrideKeyFrame, IAMVideoCompressionOverrideKeyFrame, OverrideKeyFrame, OverrideKeyFrame method [DirectShow], OverrideKeyFrame method [DirectShow],IAMVideoCompression interface, dshow.iamvideocompression_overridekeyframe, strmif/IAMVideoCompression::OverrideKeyFrame
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
 - IAMVideoCompression.OverrideKeyFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMVideoCompression.OverrideKeyFrame
: 
---

# IAMVideoCompression::OverrideKeyFrame


## -description



The <code>OverrideKeyFrame</code> method instructs the filter to compress a particular frame as a key frame.




## -parameters




### -param FrameNumber [in]

Specifies the frame number. The first frame that the filter delivers is numbered zero.


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
</table>
 




## -remarks



If the filter supports this method, you can use it to override the normal key-frame distribution for a particular frame. After the filter creates a key frame, it might reset its count to determine when the next key frame should occur. For example, if the key-frame rate is 10, and an application uses this method to force frame 5 as a key frame, the filter might wait another 10 frames (until frame 15) before it creates the next key frame.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>
 

 

