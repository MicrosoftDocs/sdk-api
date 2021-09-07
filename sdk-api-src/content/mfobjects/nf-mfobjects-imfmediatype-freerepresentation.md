---
UID: NF:mfobjects.IMFMediaType.FreeRepresentation
title: IMFMediaType::FreeRepresentation (mfobjects.h)
description: Frees memory that was allocated by the IMFMediaType::GetRepresentation method.
helpviewer_keywords: ["FreeRepresentation","FreeRepresentation method [Media Foundation]","FreeRepresentation method [Media Foundation]","IMFMediaType interface","IMFMediaType interface [Media Foundation]","FreeRepresentation method","IMFMediaType.FreeRepresentation","IMFMediaType::FreeRepresentation","d2007f16-543f-4f05-a44d-b4b4ae8019fb","mf.imfmediatype_freerepresentation","mfobjects/IMFMediaType::FreeRepresentation"]
old-location: mf\imfmediatype_freerepresentation.htm
tech.root: mf
ms.assetid: d2007f16-543f-4f05-a44d-b4b4ae8019fb
ms.date: 12/05/2018
ms.keywords: FreeRepresentation, FreeRepresentation method [Media Foundation], FreeRepresentation method [Media Foundation],IMFMediaType interface, IMFMediaType interface [Media Foundation],FreeRepresentation method, IMFMediaType.FreeRepresentation, IMFMediaType::FreeRepresentation, d2007f16-543f-4f05-a44d-b4b4ae8019fb, mf.imfmediatype_freerepresentation, mfobjects/IMFMediaType::FreeRepresentation
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFMediaType::FreeRepresentation
 - mfobjects/IMFMediaType::FreeRepresentation
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
 - IMFMediaType.FreeRepresentation
---

# IMFMediaType::FreeRepresentation


## -description

Frees memory that was allocated by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">IMFMediaType::GetRepresentation</a> method.

## -parameters

### -param guidRepresentation [in]

GUID that was passed to the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">GetRepresentation</a> method.

### -param pvRepresentation [in]

Pointer to the buffer that was returned by the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation">GetRepresentation</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>