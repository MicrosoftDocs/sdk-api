---
UID: NF:strmif.IIPDVDec.put_IPDisplay
title: IIPDVDec::put_IPDisplay (strmif.h)
description: The put_IPDisplay method sets the decoding resolution.
helpviewer_keywords: ["IIPDVDec interface [DirectShow]","put_IPDisplay method","IIPDVDec.put_IPDisplay","IIPDVDec::put_IPDisplay","IIPDVDecput_IPDisplay","dshow.iipdvdec_put_ipdisplay","put_IPDisplay","put_IPDisplay method [DirectShow]","put_IPDisplay method [DirectShow]","IIPDVDec interface","strmif/IIPDVDec::put_IPDisplay"]
old-location: dshow\iipdvdec_put_ipdisplay.htm
tech.root: dshow
ms.assetid: c89970f8-b515-409b-af75-b1af65a8f94e
ms.date: 12/05/2018
ms.keywords: IIPDVDec interface [DirectShow],put_IPDisplay method, IIPDVDec.put_IPDisplay, IIPDVDec::put_IPDisplay, IIPDVDecput_IPDisplay, dshow.iipdvdec_put_ipdisplay, put_IPDisplay, put_IPDisplay method [DirectShow], put_IPDisplay method [DirectShow],IIPDVDec interface, strmif/IIPDVDec::put_IPDisplay
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
 - IIPDVDec::put_IPDisplay
 - strmif/IIPDVDec::put_IPDisplay
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
 - IIPDVDec.put_IPDisplay
---

# IIPDVDec::put_IPDisplay


## -description

The <code>put_IPDisplay</code> method sets the decoding resolution.

## -parameters

### -param displayPix [in]

Member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvresolution">DVDECODERRESOLUTION</a> enumerated type, specifying the decoding resolution. The meaning of this value depends on whether the current format is NTSC or PAL. The filter determines at run time which format applies, based on the media type.

## -returns

Returns S_OK if successful; otherwise, returns E_FAIL or another error code.

## -remarks

This method will fail if the filter is already streaming media data.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iipdvdec">IIPDVDec Interface</a>