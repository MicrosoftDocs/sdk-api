---
UID: NF:mftransform.IMFTransform.GetStreamCount
title: IMFTransform::GetStreamCount (mftransform.h)
description: Gets the current number of input and output streams on this Media Foundation transform (MFT).
helpviewer_keywords: ["491f7f44-fcac-4236-ba5c-e5705267c6c2","GetStreamCount","GetStreamCount method [Media Foundation]","GetStreamCount method [Media Foundation]","IMFTransform interface","IMFTransform interface [Media Foundation]","GetStreamCount method","IMFTransform.GetStreamCount","IMFTransform::GetStreamCount","mf.imftransform_getstreamcount","mftransform/IMFTransform::GetStreamCount"]
old-location: mf\imftransform_getstreamcount.htm
tech.root: mf
ms.assetid: 491f7f44-fcac-4236-ba5c-e5705267c6c2
ms.date: 12/05/2018
ms.keywords: 491f7f44-fcac-4236-ba5c-e5705267c6c2, GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetStreamCount method, IMFTransform.GetStreamCount, IMFTransform::GetStreamCount, mf.imftransform_getstreamcount, mftransform/IMFTransform::GetStreamCount
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTransform::GetStreamCount
 - mftransform/IMFTransform::GetStreamCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTransform.GetStreamCount
---

# IMFTransform::GetStreamCount


## -description

Gets the current number of input and output streams on this Media Foundation transform (MFT).

## -parameters

### -param pcInputStreams [out]

Receives the number of input streams.

### -param pcOutputStreams [out]

Receives the number of output streams.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The number of streams includes unselected streams—that is, streams with no media type or a <b>NULL</b> media type.

This method should not be called with <b>NULL</b> parameters, although in practice some implementations may allow <b>NULL</b> parameters.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamCount</b>. See <a href="/windows/desktop/medfound/comparison-of-mfts-and-dmos">Creating Hybrid DMO/MFT Objects</a>.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>