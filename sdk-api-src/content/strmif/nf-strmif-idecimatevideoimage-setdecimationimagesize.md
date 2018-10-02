---
UID: NF:strmif.IDecimateVideoImage.SetDecimationImageSize
title: IDecimateVideoImage::SetDecimationImageSize
author: windows-sdk-content
description: The SetDecimationImageSize method specifies the dimensions to which the decoder should decimate its output image.
old-location: dshow\idecimatevideoimage_setdecimationimagesize.htm
tech.root: DirectShow
ms.assetid: 3f165e74-768f-48e3-be0f-887962ea9bfb
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDecimateVideoImage interface [DirectShow],SetDecimationImageSize method, IDecimateVideoImage.SetDecimationImageSize, IDecimateVideoImage::SetDecimationImageSize, IDecimateVideoImageSetDecimationImageSize, SetDecimationImageSize, SetDecimationImageSize method [DirectShow], SetDecimationImageSize method [DirectShow],IDecimateVideoImage interface, dshow.idecimatevideoimage_setdecimationimagesize, strmif/IDecimateVideoImage::SetDecimationImageSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDecimateVideoImage.SetDecimationImageSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDecimateVideoImage::SetDecimationImageSize


## -description



The <code>SetDecimationImageSize</code> method specifies the dimensions to which the decoder should decimate its output image.




## -parameters




### -param lWidth [in]

Specifies the width of the video image, in pixels.


### -param lHeight [in]

Specifies the height of the video image, in pixels.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The decoder cannot perform any decimation, or needs to halt decimation it is currently performing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The decoder can decimate the video to the requested size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0d338d41-546f-41da-bc1f-b1dd74b399ef">IDecimateVideoImage Interface</a>
 

 

