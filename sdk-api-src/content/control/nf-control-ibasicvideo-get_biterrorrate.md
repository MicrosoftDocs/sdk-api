---
UID: NF:control.IBasicVideo.get_BitErrorRate
title: IBasicVideo::get_BitErrorRate (control.h)
description: The get_BitErrorRate method retrieves the approximate bit error rate of the video stream.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_BitErrorRate method","IBasicVideo.get_BitErrorRate","IBasicVideo::get_BitErrorRate","IBasicVideoget_BitErrorRate","control/IBasicVideo::get_BitErrorRate","dshow.ibasicvideo_get_biterrorrate","get_BitErrorRate","get_BitErrorRate method [DirectShow]","get_BitErrorRate method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_biterrorrate.htm
tech.root: dshow
ms.assetid: c61b8a96-83ea-49e2-884e-c9fb3526cc46
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],get_BitErrorRate method, IBasicVideo.get_BitErrorRate, IBasicVideo::get_BitErrorRate, IBasicVideoget_BitErrorRate, control/IBasicVideo::get_BitErrorRate, dshow.ibasicvideo_get_biterrorrate, get_BitErrorRate, get_BitErrorRate method [DirectShow], get_BitErrorRate method [DirectShow],IBasicVideo interface
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
 - IBasicVideo::get_BitErrorRate
 - control/IBasicVideo::get_BitErrorRate
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
 - IBasicVideo.get_BitErrorRate
---

# IBasicVideo::get_BitErrorRate


## -description

The <code>get_BitErrorRate</code> method retrieves the approximate bit error rate of the video stream

## -parameters

### -param pBitErrorRate [out]

Pointer to a variable that receives the approximate number of bits per error.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>