---
UID: NF:control.IBasicVideo.SetSourcePosition
title: IBasicVideo::SetSourcePosition (control.h)
description: The SetSourcePosition method sets the source rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","SetSourcePosition method","IBasicVideo.SetSourcePosition","IBasicVideo::SetSourcePosition","IBasicVideoSetSourcePosition","SetSourcePosition","SetSourcePosition method [DirectShow]","SetSourcePosition method [DirectShow]","IBasicVideo interface","control/IBasicVideo::SetSourcePosition","dshow.ibasicvideo_setsourceposition"]
old-location: dshow\ibasicvideo_setsourceposition.htm
tech.root: dshow
ms.assetid: afe78775-f2b0-4d10-a702-f0329fe79c6d
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],SetSourcePosition method, IBasicVideo.SetSourcePosition, IBasicVideo::SetSourcePosition, IBasicVideoSetSourcePosition, SetSourcePosition, SetSourcePosition method [DirectShow], SetSourcePosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetSourcePosition, dshow.ibasicvideo_setsourceposition
req.header: control.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBasicVideo::SetSourcePosition
 - control/IBasicVideo::SetSourcePosition
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
 - IBasicVideo.SetSourcePosition
---

# IBasicVideo::SetSourcePosition


## -description

The <code>SetSourcePosition</code> method sets the source rectangle.

## -parameters

### -param Left [in]

Specifies the x-coordinate, in pixels.

### -param Top [in]

Specifies the y-coordinate, in pixels.

### -param Width [in]

Specifies the width, in pixels.

### -param Height [in]

Specifies the height, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method has the same effect as individually calling the <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_sourceleft">IBasicVideo::put_SourceLeft</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_sourcetop">IBasicVideo::put_SourceTop</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_sourcewidth">IBasicVideo::put_SourceWidth</a>, and <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_sourceheight">IBasicVideo::put_SourceHeight</a> methods.

Setting this coordinate does not affect the destination rectangle height.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>