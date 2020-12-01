---
UID: NF:bits.IBackgroundCopyJob.GetErrorCount
title: IBackgroundCopyJob::GetErrorCount (bits.h)
description: Retrieves the number of times BITS tried to transfer the job and an error occurred.
helpviewer_keywords: ["GetErrorCount","GetErrorCount method [BITS]","GetErrorCount method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetErrorCount method","IBackgroundCopyJob.GetErrorCount","IBackgroundCopyJob::GetErrorCount","_drz_ibackgroundcopyjob_geterrorcount","bits.ibackgroundcopyjob_geterrorcount","bits/IBackgroundCopyJob::GetErrorCount"]
old-location: bits\ibackgroundcopyjob_geterrorcount.htm
tech.root: Bits
ms.assetid: 04ca4752-8c4d-4f54-9dfa-3c9f567d7980
ms.date: 12/05/2018
ms.keywords: GetErrorCount, GetErrorCount method [BITS], GetErrorCount method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetErrorCount method, IBackgroundCopyJob.GetErrorCount, IBackgroundCopyJob::GetErrorCount, _drz_ibackgroundcopyjob_geterrorcount, bits.ibackgroundcopyjob_geterrorcount, bits/IBackgroundCopyJob::GetErrorCount
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
 - IBackgroundCopyJob::GetErrorCount
 - bits/IBackgroundCopyJob::GetErrorCount
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
 - IBackgroundCopyJob.GetErrorCount
---

# IBackgroundCopyJob::GetErrorCount


## -description

Retrieves the number of times BITS tried to transfer the job and an error occurred.

## -parameters

### -param Errors [out]

Number of errors that occurred while BITS tried to transfer the job. The count increases  when the job moves from the BG_JOB_STATE_TRANSFERRING state to the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -remarks

The count is never reset. The count may not accurately reflect the number of times the job moves to the transient error or error state. For example, BITS does not increase the count when network disconnects occur, the check disk program runs, or the bandwidth policy prevents jobs from transferring. 

BITS also increases the count each time it tries to transfer the job when the job is in the transient error state and the job fails.

<b>BITS 1.5 and earlier:  </b> BITS does not increase the count each time it tries to transfer the job when it is in the transient error state.

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-geterror">IBackgroundCopyJob::GetError</a>