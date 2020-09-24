---
UID: NF:strmif.IAMVfwCompressDialogs.GetState
title: IAMVfwCompressDialogs::GetState (strmif.h)
description: The GetState method retrieves the current configuration settings for the VCM codec currently being used.
helpviewer_keywords: ["GetState","GetState method [DirectShow]","GetState method [DirectShow]","IAMVfwCompressDialogs interface","IAMVfwCompressDialogs interface [DirectShow]","GetState method","IAMVfwCompressDialogs.GetState","IAMVfwCompressDialogs::GetState","IAMVfwCompressDialogsGetState","dshow.iamvfwcompressdialogs_getstate","strmif/IAMVfwCompressDialogs::GetState"]
old-location: dshow\iamvfwcompressdialogs_getstate.htm
tech.root: dshow
ms.assetid: a010fd8a-ad4a-4b52-abfe-a2db8cd15b65
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IAMVfwCompressDialogs interface, IAMVfwCompressDialogs interface [DirectShow],GetState method, IAMVfwCompressDialogs.GetState, IAMVfwCompressDialogs::GetState, IAMVfwCompressDialogsGetState, dshow.iamvfwcompressdialogs_getstate, strmif/IAMVfwCompressDialogs::GetState
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
 - IAMVfwCompressDialogs::GetState
 - strmif/IAMVfwCompressDialogs::GetState
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
 - IAMVfwCompressDialogs.GetState
---

# IAMVfwCompressDialogs::GetState


## -description

The <code>GetState</code> method retrieves the current configuration settings for the VCM codec currently being used.

## -parameters

### -param pState [out]

State of the VCM codec.

### -param pcbState [in, out]

Pointer to the size of the state.

## -returns

Return value varies depending on the implementation within each driver.

## -remarks

This method calls the  <a href="/windows/desktop/api/vfw/nf-vfw-icgetstate">ICGetState</a> macro.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvfwcompressdialogs">IAMVfwCompressDialogs Interface</a>