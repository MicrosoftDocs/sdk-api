---
UID: NF:strmif.IMediaSample.SetPreroll
title: IMediaSample::SetPreroll (strmif.h)
description: The SetPreroll method specifies whether this sample is a preroll sample.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetPreroll method","IMediaSample.SetPreroll","IMediaSample::SetPreroll","IMediaSampleSetPreroll","SetPreroll","SetPreroll method [DirectShow]","SetPreroll method [DirectShow]","IMediaSample interface","dshow.imediasample_setpreroll","strmif/IMediaSample::SetPreroll"]
old-location: dshow\imediasample_setpreroll.htm
tech.root: dshow
ms.assetid: a92f2774-19ac-4630-ad66-2299336d1338
ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],SetPreroll method, IMediaSample.SetPreroll, IMediaSample::SetPreroll, IMediaSampleSetPreroll, SetPreroll, SetPreroll method [DirectShow], SetPreroll method [DirectShow],IMediaSample interface, dshow.imediasample_setpreroll, strmif/IMediaSample::SetPreroll
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaSample::SetPreroll
 - strmif/IMediaSample::SetPreroll
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
 - IMediaSample.SetPreroll
---

# IMediaSample::SetPreroll


## -description

The <code>SetPreroll</code> method specifies whether this sample is a preroll sample.

## -parameters

### -param bIsPreroll

Boolean value that specifies whether this is a preroll sample. If <b>TRUE</b>, this is a preroll sample.

## -returns

Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediasample-ispreroll">IMediaSample::IsPreroll</a>