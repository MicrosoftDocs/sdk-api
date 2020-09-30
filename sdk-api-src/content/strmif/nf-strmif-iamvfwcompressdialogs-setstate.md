---
UID: NF:strmif.IAMVfwCompressDialogs.SetState
title: IAMVfwCompressDialogs::SetState (strmif.h)
description: The SetState method sets configuration for the VCM codec.
helpviewer_keywords: ["IAMVfwCompressDialogs interface [DirectShow]","SetState method","IAMVfwCompressDialogs.SetState","IAMVfwCompressDialogs::SetState","IAMVfwCompressDialogsSetState","SetState","SetState method [DirectShow]","SetState method [DirectShow]","IAMVfwCompressDialogs interface","dshow.iamvfwcompressdialogs_setstate","strmif/IAMVfwCompressDialogs::SetState"]
old-location: dshow\iamvfwcompressdialogs_setstate.htm
tech.root: dshow
ms.assetid: 9b27bbaa-4e2f-4567-a6fc-62fb3f5f31a8
ms.date: 12/05/2018
ms.keywords: IAMVfwCompressDialogs interface [DirectShow],SetState method, IAMVfwCompressDialogs.SetState, IAMVfwCompressDialogs::SetState, IAMVfwCompressDialogsSetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IAMVfwCompressDialogs interface, dshow.iamvfwcompressdialogs_setstate, strmif/IAMVfwCompressDialogs::SetState
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
 - IAMVfwCompressDialogs::SetState
 - strmif/IAMVfwCompressDialogs::SetState
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
 - IAMVfwCompressDialogs.SetState
---

# IAMVfwCompressDialogs::SetState


## -description

The <code>SetState</code> method sets configuration for the VCM codec.

## -parameters

### -param pState [in]

State of the VCM codec.

### -param cbState [in]

Size of the state.

## -returns

Return value varies depending on the implementation within each driver.

## -remarks

This method calls the <a href="/windows/desktop/api/vfw/nf-vfw-icsetstate">ICSetState</a> macro, which notifies a video compression driver to set the state of the compressor.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcompressdialogs">IAMVfwCompressDialogs Interface</a>