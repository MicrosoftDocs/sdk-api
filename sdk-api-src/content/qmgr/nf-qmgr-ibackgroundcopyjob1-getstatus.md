---
UID: NF:qmgr.IBackgroundCopyJob1.GetStatus
title: IBackgroundCopyJob1::GetStatus (qmgr.h)
description: Use the GetStatus method to retrieve the state of the job.
helpviewer_keywords: ["GetStatus","GetStatus method [BITS]","GetStatus method [BITS]","IBackgroundCopyJob1 interface","IBackgroundCopyJob1 interface [BITS]","GetStatus method","IBackgroundCopyJob1.GetStatus","IBackgroundCopyJob1::GetStatus","QM_STATUS_JOB_COMPLETE","QM_STATUS_JOB_ERROR","QM_STATUS_JOB_FOREGROUND","QM_STATUS_JOB_INCOMPLETE","bits.ibackgroundcopyjob1_getstatus","qmgr/IBackgroundCopyJob1::GetStatus"]
old-location: bits\ibackgroundcopyjob1_getstatus.htm
tech.root: Bits
ms.assetid: 6a4530fd-6b8e-4f31-a16e-5ed40adb4957
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [BITS], GetStatus method [BITS],IBackgroundCopyJob1 interface, IBackgroundCopyJob1 interface [BITS],GetStatus method, IBackgroundCopyJob1.GetStatus, IBackgroundCopyJob1::GetStatus, QM_STATUS_JOB_COMPLETE, QM_STATUS_JOB_ERROR, QM_STATUS_JOB_FOREGROUND, QM_STATUS_JOB_INCOMPLETE, bits.ibackgroundcopyjob1_getstatus, qmgr/IBackgroundCopyJob1::GetStatus
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
 - IBackgroundCopyJob1::GetStatus
 - qmgr/IBackgroundCopyJob1::GetStatus
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
 - IBackgroundCopyJob1.GetStatus
---

# IBackgroundCopyJob1::GetStatus


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>GetStatus</b> method to retrieve the state of the job.

## -parameters

### -param pdwStatus [out]

State of the job. The state can be set to one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_JOB_FOREGROUND"></a><a id="qm_status_job_foreground"></a><dl>
<dt><b>QM_STATUS_JOB_FOREGROUND</b></dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_JOB_INCOMPLETE"></a><a id="qm_status_job_incomplete"></a><dl>
<dt><b>QM_STATUS_JOB_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
QMGR is still downloading the job.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_JOB_COMPLETE"></a><a id="qm_status_job_complete"></a><dl>
<dt><b>QM_STATUS_JOB_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The job is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="QM_STATUS_JOB_ERROR"></a><a id="qm_status_job_error"></a><dl>
<dt><b>QM_STATUS_JOB_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while processing the job. 

</td>
</tr>
</table>

### -param pdwWin32Result [out]

Win32 error code. Valid only if the QM_STATUS_JOB_ERROR <i>dwStatus</i> flag is set.

### -param pdwTransportResult [out]

HTTP error code. Valid only if the QM_STATUS_JOB_ERROR <i>dwStatus</i> flag is set.

### -param pdwNumOfRetries [out]

Number of times QMGR tried to download the job after an error occurs. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.

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
Successfully retrieved the state of the job.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>