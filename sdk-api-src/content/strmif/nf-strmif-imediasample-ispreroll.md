---
UID: NF:strmif.IMediaSample.IsPreroll
title: IMediaSample::IsPreroll (strmif.h)
description: The IsPreroll method determines if this sample is a preroll sample. A preroll sample should not be displayed.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","IsPreroll method","IMediaSample.IsPreroll","IMediaSample::IsPreroll","IMediaSampleIsPreroll","IsPreroll","IsPreroll method [DirectShow]","IsPreroll method [DirectShow]","IMediaSample interface","dshow.imediasample_ispreroll","strmif/IMediaSample::IsPreroll"]
old-location: dshow\imediasample_ispreroll.htm
tech.root: dshow
ms.assetid: 7df1d34f-ba55-42bd-b61b-272ef72e13a8
ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],IsPreroll method, IMediaSample.IsPreroll, IMediaSample::IsPreroll, IMediaSampleIsPreroll, IsPreroll, IsPreroll method [DirectShow], IsPreroll method [DirectShow],IMediaSample interface, dshow.imediasample_ispreroll, strmif/IMediaSample::IsPreroll
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
 - IMediaSample::IsPreroll
 - strmif/IMediaSample::IsPreroll
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
 - IMediaSample.IsPreroll
---

# IMediaSample::IsPreroll


## -description

The <code>IsPreroll</code> method determines if this sample is a preroll sample. A preroll sample should not be displayed.



## -returns

Returns S_OK if the sample is a preroll sample. Otherwise, returns S_FALSE.

## -remarks

Preroll samples are processed but not displayed. They are located in the media stream before the displayable samples.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
