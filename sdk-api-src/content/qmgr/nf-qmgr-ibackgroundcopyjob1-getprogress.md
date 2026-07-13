---
UID: NF:qmgr.IBackgroundCopyJob1.GetProgress
title: IBackgroundCopyJob1::GetProgress (qmgr.h)
description: Use the GetProgress method to retrieve the job's progress.
helpviewer_keywords: ["GetProgress","GetProgress method [BITS]","GetProgress method [BITS]","IBackgroundCopyJob1 interface","IBackgroundCopyJob1 interface [BITS]","GetProgress method","IBackgroundCopyJob1.GetProgress","IBackgroundCopyJob1::GetProgress","QM_PROGRESS_PERCENT_DONE","QM_PROGRESS_SIZE_DONE","QM_PROGRESS_TIME_DONE","bits.ibackgroundcopyjob1_getprogress","qmgr/IBackgroundCopyJob1::GetProgress"]
old-location: bits\ibackgroundcopyjob1_getprogress.htm
tech.root: Bits
ms.assetid: 4d4444b6-e40a-4138-9462-49809ec84ccd
ms.date: 12/05/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],GetProgress method, IBackgroundCopyJob1.GetProgress, IBackgroundCopyJob1::GetProgress, QM_PROGRESS_PERCENT_DONE, QM_PROGRESS_SIZE_DONE, QM_PROGRESS_TIME_DONE, bits.ibackgroundcopyjob1_getprogress, qmgr/IBackgroundCopyJob1::GetProgress
req.header: qmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Qmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob1::GetProgress
 - qmgr/IBackgroundCopyJob1::GetProgress
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
 - IBackgroundCopyJob1.GetProgress
---

# IBackgroundCopyJob1::GetProgress


## -description

<p class="CCE_Message">[<b>IBackgroundCopyJob1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetProgress</b> method to retrieve the job's progress.

## -parameters

### -param dwFlags [in]

Type of progress to retrieve. Specify one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_PERCENT_DONE"></a><a id="qm_progress_percent_done"></a><dl>
<dt><b>QM_PROGRESS_PERCENT_DONE</b></dt>
</dl>
</td>
<td width="60%">
Returns the percent of the download that is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_SIZE_DONE"></a><a id="qm_progress_size_done"></a><dl>
<dt><b>QM_PROGRESS_SIZE_DONE</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of bytes downloaded.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_PROGRESS_TIME_DONE"></a><a id="qm_progress_time_done"></a><dl>
<dt><b>QM_PROGRESS_TIME_DONE</b></dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
</table>

### -param pdwProgress [out]

Progress of the download. The progress represents the number of bytes downloaded or the percent of the download that is complete, depending on <i>dwFlags</i>.

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
Successfully retrieved the job's progress.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
You cannot specify QM_PROGRESS_TIME_DONE for the <i>dwFlags</i> parameter.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>