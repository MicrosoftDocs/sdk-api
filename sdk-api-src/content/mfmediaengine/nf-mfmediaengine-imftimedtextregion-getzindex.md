---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetZIndex
title: IMFTimedTextRegion::GetZIndex (mfmediaengine.h)
description: Gets the Z-index (depth) of the region.
helpviewer_keywords: ["GetZIndex","GetZIndex method [Media Foundation]","GetZIndex method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetZIndex method","IMFTimedTextRegion.GetZIndex","IMFTimedTextRegion::GetZIndex","mf.imftimedtextregion_getzindex","mfmediaengine/IMFTimedTextRegion::GetZIndex"]
old-location: mf\imftimedtextregion_getzindex.htm
tech.root: medfound
ms.assetid: 662A5D79-7FCE-45D3-BCB1-5DE08DC0F981
ms.date: 12/05/2018
ms.keywords: GetZIndex, GetZIndex method [Media Foundation], GetZIndex method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetZIndex method, IMFTimedTextRegion.GetZIndex, IMFTimedTextRegion::GetZIndex, mf.imftimedtextregion_getzindex, mfmediaengine/IMFTimedTextRegion::GetZIndex
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimedTextRegion::GetZIndex
 - mfmediaengine/IMFTimedTextRegion::GetZIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextRegion.GetZIndex
---

# IMFTimedTextRegion::GetZIndex


## -description

Gets the Z-index (depth) of the region.

## -parameters

### -param zIndex [out]

Type: <b>INT32*</b>

A pointer to a variable that receives the Z-index (depth) of the region.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>