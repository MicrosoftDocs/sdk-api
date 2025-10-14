---
UID: NF:bits.IBackgroundCopyJob.GetTimes
title: IBackgroundCopyJob::GetTimes (bits.h)
description: Retrieves job-related time stamps, such as the time that the job was created or last modified.
helpviewer_keywords: ["GetTimes","GetTimes method [BITS]","GetTimes method [BITS]","IBackgroundCopyJob interface","IBackgroundCopyJob interface [BITS]","GetTimes method","IBackgroundCopyJob.GetTimes","IBackgroundCopyJob::GetTimes","_drz_ibackgroundcopyjob_gettimes","bits.ibackgroundcopyjob_gettimes","bits/IBackgroundCopyJob::GetTimes"]
old-location: bits\ibackgroundcopyjob_gettimes.htm
tech.root: Bits
ms.assetid: acc29cc2-b437-4799-9cdb-388a60f117e9
ms.date: 12/05/2018
ms.keywords: GetTimes, GetTimes method [BITS], GetTimes method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetTimes method, IBackgroundCopyJob.GetTimes, IBackgroundCopyJob::GetTimes, _drz_ibackgroundcopyjob_gettimes, bits.ibackgroundcopyjob_gettimes, bits/IBackgroundCopyJob::GetTimes
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
 - IBackgroundCopyJob::GetTimes
 - bits/IBackgroundCopyJob::GetTimes
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
 - IBackgroundCopyJob.GetTimes
---

# IBackgroundCopyJob::GetTimes


## -description

Retrieves job-related time stamps, such as the time that the job was created or last modified.

## -parameters

### -param pVal [out]

Contains job-related time stamps. For available time stamps, see the 
<a href="/windows/desktop/api/bits/ns-bits-bg_job_times">BG_JOB_TIMES</a> structure.

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
Time stamps were successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTimes</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bits/ns-bits-bg_job_times">BG_JOB_TIMES</a>