---
UID: NF:bits.IBackgroundCopyJob.GetMinimumRetryDelay
title: IBackgroundCopyJob::GetMinimumRetryDelay (bits.h)
description: Retrieves the minimum length of time that the service waits after encountering a transient error condition before trying to transfer the file.
helpviewer_keywords: ["GetMinimumRetryDelay","GetMinimumRetryDelay method [BITS]","GetMinimumRetryDelay method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetMinimumRetryDelay method","IBackgroundCopyJob.GetMinimumRetryDelay","IBackgroundCopyJob::GetMinimumRetryDelay","_drz_ibackgroundcopyjob_getminimumretrydelay","bits.ibackgroundcopyjob_getminimumretrydelay","bits/IBackgroundCopyJob::GetMinimumRetryDelay"]
old-location: bits\ibackgroundcopyjob_getminimumretrydelay.htm
tech.root: Bits
ms.assetid: af599174-44f8-4d5e-b9ff-61ddbb330580
ms.date: 12/05/2018
ms.keywords: GetMinimumRetryDelay, GetMinimumRetryDelay method [BITS], GetMinimumRetryDelay method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetMinimumRetryDelay method, IBackgroundCopyJob.GetMinimumRetryDelay, IBackgroundCopyJob::GetMinimumRetryDelay, _drz_ibackgroundcopyjob_getminimumretrydelay, bits.ibackgroundcopyjob_getminimumretrydelay, bits/IBackgroundCopyJob::GetMinimumRetryDelay
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob::GetMinimumRetryDelay
 - bits/IBackgroundCopyJob::GetMinimumRetryDelay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetMinimumRetryDelay
---

# IBackgroundCopyJob::GetMinimumRetryDelay


## -description

Retrieves the minimum length of time that the service waits after encountering a transient error condition before trying to transfer the file.

## -parameters

### -param Seconds [in]

Length of time, in seconds, that the service waits after encountering a transient error before trying to transfer the file.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout">IBackgroundCopyJob::GetNoProgressTimeout</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay">IBackgroundCopyJob::SetMinimumRetryDelay</a>