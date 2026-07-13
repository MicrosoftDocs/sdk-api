---
UID: NF:mfapi.MFUnwrapMediaType
title: MFUnwrapMediaType function (mfapi.h)
description: Retrieves a media type that was wrapped in another media type by the MFWrapMediaType function.
helpviewer_keywords: ["2cb6a5ae-315f-4de2-8817-da9d41db14b8","MFUnwrapMediaType","MFUnwrapMediaType function [Media Foundation]","mf.mfunwrapmediatype","mfapi/MFUnwrapMediaType"]
old-location: mf\mfunwrapmediatype.htm
tech.root: mf
ms.assetid: 2cb6a5ae-315f-4de2-8817-da9d41db14b8
ms.date: 12/05/2018
ms.keywords: 2cb6a5ae-315f-4de2-8817-da9d41db14b8, MFUnwrapMediaType, MFUnwrapMediaType function [Media Foundation], mf.mfunwrapmediatype, mfapi/MFUnwrapMediaType
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
 - MFUnwrapMediaType
 - mfapi/MFUnwrapMediaType
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
 - MFUnwrapMediaType
---

# MFUnwrapMediaType function


## -description

Retrieves a media type that was wrapped in another media type by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype">MFWrapMediaType</a> function.

## -parameters

### -param pWrap

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type that was retrieved by <a href="/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype">MFWrapMediaType</a>.

### -param ppOrig

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the original media type. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>