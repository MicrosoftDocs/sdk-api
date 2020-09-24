---
UID: NF:strmif.IDecimateVideoImage.SetDecimationImageSize
title: IDecimateVideoImage::SetDecimationImageSize (strmif.h)
description: The SetDecimationImageSize method specifies the dimensions to which the decoder should decimate its output image.
helpviewer_keywords: ["IDecimateVideoImage interface [DirectShow]","SetDecimationImageSize method","IDecimateVideoImage.SetDecimationImageSize","IDecimateVideoImage::SetDecimationImageSize","IDecimateVideoImageSetDecimationImageSize","SetDecimationImageSize","SetDecimationImageSize method [DirectShow]","SetDecimationImageSize method [DirectShow]","IDecimateVideoImage interface","dshow.idecimatevideoimage_setdecimationimagesize","strmif/IDecimateVideoImage::SetDecimationImageSize"]
old-location: dshow\idecimatevideoimage_setdecimationimagesize.htm
tech.root: dshow
ms.assetid: 3f165e74-768f-48e3-be0f-887962ea9bfb
ms.date: 12/05/2018
ms.keywords: IDecimateVideoImage interface [DirectShow],SetDecimationImageSize method, IDecimateVideoImage.SetDecimationImageSize, IDecimateVideoImage::SetDecimationImageSize, IDecimateVideoImageSetDecimationImageSize, SetDecimationImageSize, SetDecimationImageSize method [DirectShow], SetDecimationImageSize method [DirectShow],IDecimateVideoImage interface, dshow.idecimatevideoimage_setdecimationimagesize, strmif/IDecimateVideoImage::SetDecimationImageSize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDecimateVideoImage::SetDecimationImageSize
 - strmif/IDecimateVideoImage::SetDecimationImageSize
dev_langs:
 - c++
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idecimatevideoimage">IDecimateVideoImage Interface</a>