---
UID: NF:control.IBasicVideo.GetVideoSize
title: IBasicVideo::GetVideoSize (control.h)
description: The GetVideoSize method retrieves the native video dimensions.
helpviewer_keywords: ["GetVideoSize","GetVideoSize method [DirectShow]","GetVideoSize method [DirectShow]","IBasicVideo interface","IBasicVideo interface [DirectShow]","GetVideoSize method","IBasicVideo.GetVideoSize","IBasicVideo::GetVideoSize","IBasicVideoGetVideoSize","control/IBasicVideo::GetVideoSize","dshow.ibasicvideo_getvideosize"]
old-location: dshow\ibasicvideo_getvideosize.htm
tech.root: dshow
ms.assetid: fbabba8b-b86b-451b-ad06-4454174ee352
ms.date: 12/05/2018
ms.keywords: GetVideoSize, GetVideoSize method [DirectShow], GetVideoSize method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetVideoSize method, IBasicVideo.GetVideoSize, IBasicVideo::GetVideoSize, IBasicVideoGetVideoSize, control/IBasicVideo::GetVideoSize, dshow.ibasicvideo_getvideosize
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
 - IBasicVideo::GetVideoSize
 - control/IBasicVideo::GetVideoSize
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
 - IBasicVideo.GetVideoSize
---

# IBasicVideo::GetVideoSize


## -description

The <code>GetVideoSize</code> method retrieves the native video dimensions.

## -parameters

### -param pWidth [out]

Pointer to a variable that receives the width of the video image, in pixels.

### -param pHeight [out]

Pointer to a variable that receives the height of the video image, in pixels.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>