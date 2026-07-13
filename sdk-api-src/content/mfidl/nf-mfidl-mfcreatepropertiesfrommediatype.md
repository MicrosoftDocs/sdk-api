---
UID: NF:mfidl.MFCreatePropertiesFromMediaType
title: MFCreatePropertiesFromMediaType function (mfidl.h)
description: Creates properties from a IMFMediaType.
helpviewer_keywords: ["MFCreatePropertiesFromMediaType","MFCreatePropertiesFromMediaType function [Media Foundation]","mf.mfcreatepropertiesfrommediatype","mfidl/MFCreatePropertiesFromMediaType"]
old-location: mf\mfcreatepropertiesfrommediatype.htm
tech.root: mf
ms.assetid: D9B639BB-285C-40BF-B111-2C5501E41CE1
ms.date: 12/05/2018
ms.keywords: MFCreatePropertiesFromMediaType, MFCreatePropertiesFromMediaType function [Media Foundation], mf.mfcreatepropertiesfrommediatype, mfidl/MFCreatePropertiesFromMediaType
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFCreatePropertiesFromMediaType
 - mfidl/MFCreatePropertiesFromMediaType
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
 - MFCreatePropertiesFromMediaType
---

# MFCreatePropertiesFromMediaType function


## -description

Creates properties from a <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>.

## -parameters

### -param pMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>