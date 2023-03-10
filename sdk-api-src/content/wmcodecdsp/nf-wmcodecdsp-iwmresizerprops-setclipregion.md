---
UID: NF:wmcodecdsp.IWMResizerProps.SetClipRegion
title: IWMResizerProps::SetClipRegion (wmcodecdsp.h)
description: Sets the source rectangle. (IWMResizerProps.SetClipRegion)
helpviewer_keywords: ["IWMResizerProps interface [Media Foundation]","SetClipRegion method","IWMResizerProps.SetClipRegion","IWMResizerProps::SetClipRegion","SetClipRegion","SetClipRegion method [Media Foundation]","SetClipRegion method [Media Foundation]","IWMResizerProps interface","codecapi.iwmresizerpropssetclipregion","mf.iwmresizerpropssetclipregion","wmcodecdsp/IWMResizerProps::SetClipRegion"]
old-location: mf\iwmresizerpropssetclipregion.htm
tech.root: mf
ms.assetid: 51a11e24-a4c3-49fb-86ec-17baa1773caf
ms.date: 12/05/2018
ms.keywords: IWMResizerProps interface [Media Foundation],SetClipRegion method, IWMResizerProps.SetClipRegion, IWMResizerProps::SetClipRegion, SetClipRegion, SetClipRegion method [Media Foundation], SetClipRegion method [Media Foundation],IWMResizerProps interface, codecapi.iwmresizerpropssetclipregion, mf.iwmresizerpropssetclipregion, wmcodecdsp/IWMResizerProps::SetClipRegion
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
 - IWMResizerProps::SetClipRegion
 - wmcodecdsp/IWMResizerProps::SetClipRegion
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
 - IWMResizerProps.SetClipRegion
---

# IWMResizerProps::SetClipRegion


## -description

Sets the source rectangle.

## -parameters

### -param lClipOriXSrc [in]

Specifies the left edge of the source rectangle, in pixels.

### -param lClipOriYSrc [in]

Specifies the top edge of the source rectangle, in pixels.

### -param lClipWidthSrc [in]

Specifies the width of the source rectangle, in pixels.

### -param lClipHeightSrc [in]

Specifies the height of the source rectangle, in pixels.

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

By default, the video resizer copies the entire video frame. When you call this method, the video resizer crops the video to the source rectangle and copies that portion to the output buffer.

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
</ul>

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops">IWMResizerProps Interface</a>
