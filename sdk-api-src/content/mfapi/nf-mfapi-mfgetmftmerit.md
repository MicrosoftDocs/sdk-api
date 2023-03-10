---
UID: NF:mfapi.MFGetMFTMerit
title: MFGetMFTMerit function (mfapi.h)
description: Gets the merit value of a hardware codec.
helpviewer_keywords: ["MFGetMFTMerit","MFGetMFTMerit function [Media Foundation]","mf.mfgetmftmerit","mfapi/MFGetMFTMerit"]
old-location: mf\mfgetmftmerit.htm
tech.root: mf
ms.assetid: 69029cf3-7f34-4bb1-8dfd-fa9a8d1a63c9
ms.date: 12/05/2018
ms.keywords: MFGetMFTMerit, MFGetMFTMerit function [Media Foundation], mf.mfgetmftmerit, mfapi/MFGetMFTMerit
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - MFGetMFTMerit
 - mfapi/MFGetMFTMerit
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
 - MFGetMFTMerit
---

# MFGetMFTMerit function


## -description

Gets the merit value of a hardware codec.

## -parameters

### -param pMFT [in, out]

A pointer to the <b>IUnknown</b> interface of the Media Foundation transform (MFT) that represents the codec.

### -param cbVerifier [in]

The size, in bytes, of the <i>verifier</i> array.

### -param verifier [in]

The address of a buffer that contains one of the following:

<ul>
<li>The class identifier (CLSID) of the MFT.</li>
<li>A null-terminated wide-character string that contains the symbol link for the underlying hardware device. Include the size of the terminating null in the value of <i>cbVerifier</i>.</li>
</ul>

### -param merit [out]

Receives the merit value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The function fails if the MFT does not represent a hardware device with a valid Output Protection Manager (OPM) certificate.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/opm-get-codec-info">OPM_GET_CODEC_INFO</a>