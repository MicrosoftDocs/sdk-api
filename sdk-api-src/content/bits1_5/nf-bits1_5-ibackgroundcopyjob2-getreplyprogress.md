---
UID: NF:bits1_5.IBackgroundCopyJob2.GetReplyProgress
title: IBackgroundCopyJob2::GetReplyProgress
description: Retrieves progress information related to the transfer of the reply data from an upload-reply job.
helpviewer_keywords: ["GetReplyProgress","GetReplyProgress method [BITS]","GetReplyProgress method [BITS]","IBackgroundCopyJob2 interface","IBackgroundCopyJob2 interface [BITS]","GetReplyProgress method","IBackgroundCopyJob2.GetReplyProgress","IBackgroundCopyJob2::GetReplyProgress","_drz_ibackgroundcopyjob2_getreplyprogress","bits.ibackgroundcopyjob2_getreplyprogress","bits1_5/IBackgroundCopyJob2::GetReplyProgress"]
old-location: bits\ibackgroundcopyjob2_getreplyprogress.htm
tech.root: Bits
ms.assetid: 76509b1a-fdfb-4236-8554-f63282bfc1b6
ms.date: 12/05/2018
ms.keywords: GetReplyProgress, GetReplyProgress method [BITS], GetReplyProgress method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetReplyProgress method, IBackgroundCopyJob2.GetReplyProgress, IBackgroundCopyJob2::GetReplyProgress, _drz_ibackgroundcopyjob2_getreplyprogress, bits.ibackgroundcopyjob2_getreplyprogress, bits1_5/IBackgroundCopyJob2::GetReplyProgress
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2::GetReplyProgress
 - bits1_5/IBackgroundCopyJob2::GetReplyProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.GetReplyProgress
---

# IBackgroundCopyJob2::GetReplyProgress


## -description

Retrieves progress information related to the transfer of the reply data from an upload-reply job.

## -parameters

### -param pProgress [out]

Contains information that you use to calculate the percentage of the reply file transfer that is complete. For more information, see 
<a href="/windows/desktop/api/bits1_5/ns-bits1_5-bg_job_reply_progress">BG_JOB_REPLY_PROGRESS</a>.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

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
Progress information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented for jobs of type <b>BG_JOB_TYPE_DOWNLOAD</b> or <b>BG_JOB_TYPE_UPLOAD</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pProgress</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/ns-bits-bg_job_progress">BG_JOB_REPLY_PROGRESS</a>