---
UID: NF:strmif.IConfigInterleaving.get_Mode
title: IConfigInterleaving::get_Mode (strmif.h)
description: The get_Mode method retrieves the interleaving quality setting.
helpviewer_keywords: ["IConfigInterleaving interface [DirectShow]","get_Mode method","IConfigInterleaving.get_Mode","IConfigInterleaving::get_Mode","IConfigInterleavingget_Mode","dshow.iconfiginterleaving_get_mode","get_Mode","get_Mode method [DirectShow]","get_Mode method [DirectShow]","IConfigInterleaving interface","strmif/IConfigInterleaving::get_Mode"]
old-location: dshow\iconfiginterleaving_get_mode.htm
tech.root: dshow
ms.assetid: 02136798-1c49-4181-ad08-d128f580dbd4
ms.date: 12/05/2018
ms.keywords: IConfigInterleaving interface [DirectShow],get_Mode method, IConfigInterleaving.get_Mode, IConfigInterleaving::get_Mode, IConfigInterleavingget_Mode, dshow.iconfiginterleaving_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::get_Mode
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
 - IConfigInterleaving::get_Mode
 - strmif/IConfigInterleaving::get_Mode
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
 - IConfigInterleaving.get_Mode
---

# IConfigInterleaving::get_Mode


## -description

The <code>get_Mode</code> method retrieves the interleaving quality setting.

## -parameters

### -param pMode [out]

Receives the interleaving quality, specified as a member of the <a href="/windows/desktop/api/strmif/ne-strmif-interleavingmode">InterleavingMode</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfiginterleaving">IConfigInterleaving Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_mode">IConfigInterleaving::put_Mode</a>