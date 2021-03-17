---
UID: NF:bits10_1.IBackgroundCopyFile6.RequestFileRanges
title: IBackgroundCopyFile6::RequestFileRanges (bits10_1.h)
description: Adds a new set of file ranges to be prioritized for download.
helpviewer_keywords: ["IBackgroundCopyFile6 interface [BITS]","RequestFileRanges method","IBackgroundCopyFile6.RequestFileRanges","IBackgroundCopyFile6::RequestFileRanges","RequestFileRanges","RequestFileRanges method [BITS]","RequestFileRanges method [BITS]","IBackgroundCopyFile6 interface","bits.ibackgroundcopyfile6_requestfileranges","bits10_1/IBackgroundCopyFile6::RequestFileRanges"]
old-location: bits\ibackgroundcopyfile6_requestfileranges.htm
tech.root: Bits
ms.assetid: C36BDE94-03AC-4F06-B17B-B8729226F8AC
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile6 interface [BITS],RequestFileRanges method, IBackgroundCopyFile6.RequestFileRanges, IBackgroundCopyFile6::RequestFileRanges, RequestFileRanges, RequestFileRanges method [BITS], RequestFileRanges method [BITS],IBackgroundCopyFile6 interface, bits.ibackgroundcopyfile6_requestfileranges, bits10_1/IBackgroundCopyFile6::RequestFileRanges
req.header: bits10_1.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_1.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyFile6::RequestFileRanges
 - bits10_1/IBackgroundCopyFile6::RequestFileRanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile6.RequestFileRanges
---

# IBackgroundCopyFile6::RequestFileRanges


## -description

Adds a new set of file ranges to be prioritized for download.

## -parameters

### -param rangeCount [in]

Specifies the size of the <i>Ranges</i> array.

### -param ranges [in]

An array of file ranges to be downloaded. Requested ranges are allowed to overlap previously downloaded (or pending) ranges. Ranges are automatically split into non-overlapping ranges.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.  <b>BG_E_INVALID_RANGE</b> is returned if any part of the requested range is outside the actual file size; <b>BG_E_RANDOM_ACCESS_NOT_SUPPORTED</b> is returned if the job is not a download job or if the server loses its ability to support download ranges.

## -remarks

<b>RequestFileRanges</b> can be requested for any download job that also meets the requirements for <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> jobs.

  
The requirements for a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job is that the transfer must be a <b>DOWNLOAD</b> job.  The job must not be <b>DYNAMIC</b> and the server must be an HTTP or HTTPS server and the server requirements for range support must all be met.
For more information, see <a href="/windows/desktop/Bits/http-requirements-for-bits-downloads">HTTP Requirements for BITS Downloads</a>.

When all of the requested ranges have been downloaded the job state will be set to <b>BG_JOB_STATE_TRANSFERRED</b> if all of the bytes of the file have been transferred.  Otherwise, the job state will be set to <b>BG_JOB_STATE_SUSPENDED</b>.

## -see-also

<a href="/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6">IBackgroundCopyFile6</a>