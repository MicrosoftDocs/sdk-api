---
UID: NF:mfapi.MFCreateMediaType
title: MFCreateMediaType function (mfapi.h)
description: Creates an empty media type.
helpviewer_keywords: ["05b0941e-03ce-4ced-9022-22b65d1c4b4c","MFCreateMediaType","MFCreateMediaType function [Media Foundation]","mf.mfcreatemediatype","mfapi/MFCreateMediaType"]
old-location: mf\mfcreatemediatype.htm
tech.root: mf
ms.assetid: 05b0941e-03ce-4ced-9022-22b65d1c4b4c
ms.date: 12/05/2018
ms.keywords: 05b0941e-03ce-4ced-9022-22b65d1c4b4c, MFCreateMediaType, MFCreateMediaType function [Media Foundation], mf.mfcreatemediatype, mfapi/MFCreateMediaType
req.header: mfapi.h
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMediaType
 - mfapi/MFCreateMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMediaType
---

# MFCreateMediaType function


## -description

Creates an empty media type.

## -parameters

### -param ppMFType

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The media type is created without any attributes.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>