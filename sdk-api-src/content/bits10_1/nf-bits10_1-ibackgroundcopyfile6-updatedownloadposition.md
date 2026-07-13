---
UID: NF:bits10_1.IBackgroundCopyFile6.UpdateDownloadPosition
title: IBackgroundCopyFile6::UpdateDownloadPosition (bits10_1.h)
description: Specifies a position to prioritize downloading missing data from.
helpviewer_keywords: ["IBackgroundCopyFile6 interface [BITS]","UpdateDownloadPosition method","IBackgroundCopyFile6.UpdateDownloadPosition","IBackgroundCopyFile6::UpdateDownloadPosition","UpdateDownloadPosition","UpdateDownloadPosition method [BITS]","UpdateDownloadPosition method [BITS]","IBackgroundCopyFile6 interface","bits.ibackgroundcopyfile6_updatedownloadposition","bits10_1/IBackgroundCopyFile6::UpdateDownloadPosition"]
old-location: bits\ibackgroundcopyfile6_updatedownloadposition.htm
tech.root: Bits
ms.assetid: 243F9D5A-32D8-4D39-A9B2-E452CF745844
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile6 interface [BITS],UpdateDownloadPosition method, IBackgroundCopyFile6.UpdateDownloadPosition, IBackgroundCopyFile6::UpdateDownloadPosition, UpdateDownloadPosition, UpdateDownloadPosition method [BITS], UpdateDownloadPosition method [BITS],IBackgroundCopyFile6 interface, bits.ibackgroundcopyfile6_updatedownloadposition, bits10_1/IBackgroundCopyFile6::UpdateDownloadPosition
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
 - IBackgroundCopyFile6::UpdateDownloadPosition
 - bits10_1/IBackgroundCopyFile6::UpdateDownloadPosition
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
 - IBackgroundCopyFile6.UpdateDownloadPosition
---

# IBackgroundCopyFile6::UpdateDownloadPosition


## -description

Specifies a position to prioritize downloading missing data from.

## -parameters

### -param offset [in]

Specifies the new position to prioritize downloading missing data from.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. It will return <b>BG_E_RANDOM_ACCESS_NOT_SUPPORTED</b> if the job does not meet the requirements of a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job.

## -remarks

<b>UpdateDownloadPosition</b> can be requested for any download job that also meets the requirements for <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> jobs.

  
The requirements for a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job is that the transfer must be a <b>DOWNLOAD</b> job.  The job must not be <b>DYNAMIC</b> and the server must be an HTTP or HTTPS server and the server requirements for range support must all be met.
For more information, see <a href="/windows/desktop/Bits/http-requirements-for-bits-downloads">HTTP Requirements for BITS Downloads</a>.

## -see-also

<a href="/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6">IBackgroundCopyFile6</a>