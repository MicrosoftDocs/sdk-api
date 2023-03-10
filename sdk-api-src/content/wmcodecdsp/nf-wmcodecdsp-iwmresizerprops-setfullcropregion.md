---
UID: NF:wmcodecdsp.IWMResizerProps.SetFullCropRegion
title: IWMResizerProps::SetFullCropRegion (wmcodecdsp.h)
description: Sets the source and destination rectangles. (IWMResizerProps.SetFullCropRegion)
helpviewer_keywords: ["IWMResizerProps interface [Media Foundation]","SetFullCropRegion method","IWMResizerProps.SetFullCropRegion","IWMResizerProps::SetFullCropRegion","SetFullCropRegion","SetFullCropRegion method [Media Foundation]","SetFullCropRegion method [Media Foundation]","IWMResizerProps interface","codecapi.iwmresizerpropssetfullcropregion","mf.iwmresizerpropssetfullcropregion","wmcodecdsp/IWMResizerProps::SetFullCropRegion"]
old-location: mf\iwmresizerpropssetfullcropregion.htm
tech.root: mf
ms.assetid: 5578b90d-3b18-47a2-b4ae-75a4749f9001
ms.date: 12/05/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetFullCropRegion method, IWMResizerProps.SetFullCropRegion, IWMResizerProps::SetFullCropRegion, SetFullCropRegion, SetFullCropRegion method [Media Foundation], SetFullCropRegion method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetfullcropregion, mf.iwmresizerpropssetfullcropregion, wmcodecdsp/IWMResizerProps::SetFullCropRegion
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
 - IWMResizerProps::SetFullCropRegion
 - wmcodecdsp/IWMResizerProps::SetFullCropRegion
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
 - IWMResizerProps.SetFullCropRegion
---

# IWMResizerProps::SetFullCropRegion


## -description

Sets the source and destination rectangles.

## -parameters

### -param lClipOriXSrc [in]

Specifies the left edge of the source rectangle, in pixels.

### -param lClipOriYSrc [in]

Specifies the top edge of the source rectangle, in pixels.

### -param lClipWidthSrc [in]

Specifies the width of the source rectangle, in pixels.

### -param lClipHeightSrc [in]

Specifies the height of the source rectangle, in pixels.

### -param lClipOriXDst [in]

Specifies the left edge of the destination rectangle, in pixels.

### -param lClipOriYDst [in]

Specifies the top edge of the destination rectangle, in pixels.

### -param lClipWidthDst [in]

Specifies the width of the destination rectangle, in pixels.

### -param lClipHeightDst [in]

Specifies the height of the destination rectangle, in pixels.

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

By default, the video resizer copies the entire video frame. When you call this method, the video resizer crops the video to the source rectangle and copies that portion to the destination rectangle.

This method is equivalent to setting the following properties:

<ul>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-src-left">MFPKEY_RESIZE_SRC_LEFT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-src-top">MFPKEY_RESIZE_SRC_TOP</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-src-width">MFPKEY_RESIZE_SRC_WIDTH</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-src-height">MFPKEY_RESIZE_SRC_HEIGHT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-dst-left">MFPKEY_RESIZE_DST_LEFT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-dst-top">MFPKEY_RESIZE_DST_TOP</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-dst-width">MFPKEY_RESIZE_DST_WIDTH</a>
</li>
<li>
<a href="/windows/desktop/medfound/mfpkey-resize-dst-height">MFPKEY_RESIZE_DST_HEIGHT</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
