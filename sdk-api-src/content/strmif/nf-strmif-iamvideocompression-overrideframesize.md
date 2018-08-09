---
UID: NF:strmif.IAMVideoCompression.OverrideFrameSize
title: IAMVideoCompression::OverrideFrameSize
author: windows-sdk-content
description: The OverrideFrameSize method overrides the frame size of a specified frame.
old-location: dshow\iamvideocompression_overrideframesize.htm
old-project: DirectShow
ms.assetid: 19f5d231-965e-4b0a-bd0b-e85b03d79c71
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMVideoCompression interface [DirectShow],OverrideFrameSize method, IAMVideoCompression.OverrideFrameSize, IAMVideoCompression::OverrideFrameSize, IAMVideoCompressionOverrideFrameSize, OverrideFrameSize, OverrideFrameSize method [DirectShow], OverrideFrameSize method [DirectShow],IAMVideoCompression interface, dshow.iamvideocompression_overrideframesize, strmif/IAMVideoCompression::OverrideFrameSize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression.OverrideFrameSize
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoCompression::OverrideFrameSize


## -description



The <code>OverrideFrameSize</code> method overrides the frame size of a specified frame.




## -parameters




### -param FrameNumber [in]

Specifies the frame number. The first frame that the filter delivers is numbered zero.


### -param Size [in]

Specifies the maximum size of the specified frame, in bytes.


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



If the filter supports this method, the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method will return the <b>CompressionCaps_CanCrunch</b> flag in the <i>pCapabilities</i> parameter. However, this flag can also indicate that the filter supports setting the bit rate, so it does not guarantee that the <code>OverrideFrameSize</code> method is supported.




## -see-also




<a href="https://msdn.microsoft.com/e964756f-1c60-42fd-8497-637d5fc005d7">CompressionCaps Enumeration</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>
 

 

