---
UID: NF:wmcodecdsp.IWMColorConvProps.SetFullCroppingParam
title: IWMColorConvProps::SetFullCroppingParam (wmcodecdsp.h)
description: Sets the source and destination rectangles. (IWMColorConvProps.SetFullCroppingParam)
helpviewer_keywords: ["IWMColorConvProps interface [Media Foundation]","SetFullCroppingParam method","IWMColorConvProps.SetFullCroppingParam","IWMColorConvProps::SetFullCroppingParam","SetFullCroppingParam","SetFullCroppingParam method [Media Foundation]","SetFullCroppingParam method [Media Foundation]","IWMColorConvProps interface","codecapi.iwmcolorconvpropssetfullcroppingparam","mf.iwmcolorconvpropssetfullcroppingparam","wmcodecdsp/IWMColorConvProps::SetFullCroppingParam"]
old-location: mf\iwmcolorconvpropssetfullcroppingparam.htm
tech.root: mf
ms.assetid: 73545bbb-6630-463d-ad58-d24937e3b546
ms.date: 12/05/2018
ms.keywords: IWMColorConvProps interface [Media Foundation],SetFullCroppingParam method, IWMColorConvProps.SetFullCroppingParam, IWMColorConvProps::SetFullCroppingParam, SetFullCroppingParam, SetFullCroppingParam method [Media Foundation], SetFullCroppingParam method [Media Foundation],IWMColorConvProps interface, codecapi.iwmcolorconvpropssetfullcroppingparam, mf.iwmcolorconvpropssetfullcroppingparam, wmcodecdsp/IWMColorConvProps::SetFullCroppingParam
req.header: wmcodecdsp.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMColorConvProps::SetFullCroppingParam
 - wmcodecdsp/IWMColorConvProps::SetFullCroppingParam
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMColorConvProps.SetFullCroppingParam
---

# IWMColorConvProps::SetFullCroppingParam


## -description

Sets the source and destination rectangles.

## -parameters

### -param lSrcCropLeft [in]

Specifies the left edge of the source rectangle, in pixels.

### -param lSrcCropTop [in]

Specifies the top edge of the source rectangle, in pixels.

### -param lDstCropLeft [in]

Specifies the left edge of the destination rectangle, in pixels.

### -param lDstCropTop [in]

Specifies the top edge of the destination rectangle, in pixels.

### -param lCropWidth [in]

Specifies the width of the source and destination rectangles, in pixels.

### -param lCropHeight [in]

Specifies the height of the source and destination rectangles, in pixels.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

By default, the color converter copies the entire video frame. When you call this method, the color converter crops the video to the source rectangle and copies that portion to the destination rectangle. 

This method is equivalent to setting the following properties:

<ul>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-srcleft">MFPKEY_COLORCONV_SRCLEFT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-srctop">MFPKEY_COLORCONV_SRCTOP</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-dstleft">MFPKEY_COLORCONV_DSTLEFT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-dsttop">MFPKEY_COLORCONV_DSTTOP</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-width">MFPKEY_COLORCONV_WIDTH</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-colorconv-height">MFPKEY_COLORCONV_HEIGHT</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops">IWMColorConvProps</a>
