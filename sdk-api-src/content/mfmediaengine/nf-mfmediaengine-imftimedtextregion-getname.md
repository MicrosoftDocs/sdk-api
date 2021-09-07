---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetName
title: IMFTimedTextRegion::GetName (mfmediaengine.h)
description: Gets the name of the region.
helpviewer_keywords: ["GetName","GetName method [Media Foundation]","GetName method [Media Foundation]","IMFTimedTextRegion interface","IMFTimedTextRegion interface [Media Foundation]","GetName method","IMFTimedTextRegion.GetName","IMFTimedTextRegion::GetName","mf.imftimedtextregion_getname","mfmediaengine/IMFTimedTextRegion::GetName"]
old-location: mf\imftimedtextregion_getname.htm
tech.root: mf
ms.assetid: 1B3C07CF-0E9C-4C7D-8F41-7A0B168967A3
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Media Foundation], GetName method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetName method, IMFTimedTextRegion.GetName, IMFTimedTextRegion::GetName, mf.imftimedtextregion_getname, mfmediaengine/IMFTimedTextRegion::GetName
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
 - IMFTimedTextRegion::GetName
 - mfmediaengine/IMFTimedTextRegion::GetName
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
 - IMFTimedTextRegion.GetName
---

# IMFTimedTextRegion::GetName


## -description

Gets the name of the region.

## -parameters

### -param name [out]

Type: <b>LPCWSTR*</b>

A pointer to a variable that receives the null-terminated wide-character string that contains the name of the region.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion">IMFTimedTextRegion</a>