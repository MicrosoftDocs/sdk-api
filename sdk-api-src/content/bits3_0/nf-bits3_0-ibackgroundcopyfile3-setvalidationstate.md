---
UID: NF:bits3_0.IBackgroundCopyFile3.SetValidationState
title: IBackgroundCopyFile3::SetValidationState (bits3_0.h)
description: Sets the validation state of this file.
helpviewer_keywords: ["IBackgroundCopyFile3 interface [BITS]","SetValidationState method","IBackgroundCopyFile3.SetValidationState","IBackgroundCopyFile3::SetValidationState","SetValidationState","SetValidationState method [BITS]","SetValidationState method [BITS]","IBackgroundCopyFile3 interface","bits.ibackgroundcopyfile3_setvalidationstate","bits3_0/IBackgroundCopyFile3::SetValidationState"]
old-location: bits\ibackgroundcopyfile3_setvalidationstate.htm
tech.root: Bits
ms.assetid: c032ce32-07a4-4ab2-ae57-f9d526d1371a
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyFile3 interface [BITS],SetValidationState method, IBackgroundCopyFile3.SetValidationState, IBackgroundCopyFile3::SetValidationState, SetValidationState, SetValidationState method [BITS], SetValidationState method [BITS],IBackgroundCopyFile3 interface, bits.ibackgroundcopyfile3_setvalidationstate, bits3_0/IBackgroundCopyFile3::SetValidationState
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
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
 - IBackgroundCopyFile3::SetValidationState
 - bits3_0/IBackgroundCopyFile3::SetValidationState
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
 - IBackgroundCopyFile3.SetValidationState
---

# IBackgroundCopyFile3::SetValidationState


## -description

Sets the validation state of this file.

## -parameters

### -param state [in]

Set to <b>TRUE</b> if the file content is valid, otherwise, <b>FALSE</b>.

## -returns

The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
You cannot validate the file until the download is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_RECORD_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The cached record associated with this file has been deleted.

</td>
</tr>
</table>

## -remarks

If you set the validation state to <b>FALSE</b> and the file was downloaded from the origin server, the job moves to the error state with an error code of BG_E_VALIDATION_FAILED and the file progress is set to zero. You can then call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method to download the file again. 

<b>BITS 3.0:  </b>Do not call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-resume">IBackgroundCopyJob::Resume</a> method to download the file again. Instead, call the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> or <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-cancel">IBackgroundCopyJob::Cancel</a> method to cleanup the current job and then create a new job to download the file.

If you set the validation state to <b>FALSE</b> and the file was downloaded from a peer, BITS removes the file from the cache, resets the file progress to zero, and downloads the file again from the origin server.

You can call this method only after BITS finishes transferring the file. To receive notification when the transfer is complete, implement the <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">IBackgroundCopyCallback2::FileTransferred</a> method.

Calling the <a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-complete">IBackgroundCopyJob::Complete</a> method implicitly validates the file.

If you validate a file in the cache and then call <a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags">IBackgroundCopyJob4::SetPeerCachingFlags</a>  to disable caching (or peer caching is disable through Group Policy), the file remains in the cache. If you disable caching before validating the file, BITS removes the file from the cache.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyfile3">IBackgroundCopyFile3</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyfile3-getvalidationstate">IBackgroundCopyFile3::GetValidationState</a>



<a href="/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacherecord-isfilevalidated">IBitsPeerCacheRecord::IsFileValidated</a>