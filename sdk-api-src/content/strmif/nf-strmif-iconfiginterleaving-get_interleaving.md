---
UID: NF:strmif.IConfigInterleaving.get_Interleaving
title: IConfigInterleaving::get_Interleaving (strmif.h)
description: The get_Interleaving method gets the audio preroll time and the frequency of interleaving for an AVI file.
helpviewer_keywords: ["IConfigInterleaving interface [DirectShow]","get_Interleaving method","IConfigInterleaving.get_Interleaving","IConfigInterleaving::get_Interleaving","IConfigInterleavingget_Interleaving","dshow.iconfiginterleaving_get_interleaving","get_Interleaving","get_Interleaving method [DirectShow]","get_Interleaving method [DirectShow]","IConfigInterleaving interface","strmif/IConfigInterleaving::get_Interleaving"]
old-location: dshow\iconfiginterleaving_get_interleaving.htm
tech.root: dshow
ms.assetid: 659aa136-c7fd-4955-913b-26f7c05325a8
ms.date: 12/05/2018
ms.keywords: IConfigInterleaving interface [DirectShow],get_Interleaving method, IConfigInterleaving.get_Interleaving, IConfigInterleaving::get_Interleaving, IConfigInterleavingget_Interleaving, dshow.iconfiginterleaving_get_interleaving, get_Interleaving, get_Interleaving method [DirectShow], get_Interleaving method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::get_Interleaving
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
 - IConfigInterleaving::get_Interleaving
 - strmif/IConfigInterleaving::get_Interleaving
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
 - IConfigInterleaving.get_Interleaving
---

# IConfigInterleaving::get_Interleaving


## -description

The <b>get_Interleaving</b> method gets the audio preroll time and the frequency of interleaving for an AVI file.

## -parameters

### -param prtInterleave [out]

Receives the approximate duration of each interleaved group of audio or video chunks.

### -param prtPreroll [out]

Receives the amount of audio data, in 100-nanosecond units, that is written to the file before the first video frame.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

For more information, see <a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_interleaving">IConfigInterleaving::put_Interleaving</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfiginterleaving">IConfigInterleaving Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_interleaving">IConfigInterleaving::put_Interleaving</a>