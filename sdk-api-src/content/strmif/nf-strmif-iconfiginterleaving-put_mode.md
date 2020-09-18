---
UID: NF:strmif.IConfigInterleaving.put_Mode
title: IConfigInterleaving::put_Mode (strmif.h)
description: The put_Mode method sets how audio samples and video frames are to be written to disk, by specifying quality of interleaving.
helpviewer_keywords: ["IConfigInterleaving interface [DirectShow]","put_Mode method","IConfigInterleaving.put_Mode","IConfigInterleaving::put_Mode","IConfigInterleavingput_Mode","dshow.iconfiginterleaving_put_mode","put_Mode","put_Mode method [DirectShow]","put_Mode method [DirectShow]","IConfigInterleaving interface","strmif/IConfigInterleaving::put_Mode"]
old-location: dshow\iconfiginterleaving_put_mode.htm
tech.root: dshow
ms.assetid: 62b06dc2-2e71-4a14-82e5-63e921a3c11f
ms.date: 12/05/2018
ms.keywords: IConfigInterleaving interface [DirectShow],put_Mode method, IConfigInterleaving.put_Mode, IConfigInterleaving::put_Mode, IConfigInterleavingput_Mode, dshow.iconfiginterleaving_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::put_Mode
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
 - IConfigInterleaving::put_Mode
 - strmif/IConfigInterleaving::put_Mode
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
 - IConfigInterleaving.put_Mode
---

# IConfigInterleaving::put_Mode


## -description

The <code>put_Mode</code> method sets how audio samples and video frames are to be written to disk, by specifying quality of interleaving.

## -parameters

### -param mode [in]

Interleaving quality setting specified in the <a href="/windows/desktop/api/strmif/ne-strmif-interleavingmode">InterleavingMode</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfiginterleaving">IConfigInterleaving Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-get_mode">IConfigInterleaving::get_Mode</a>