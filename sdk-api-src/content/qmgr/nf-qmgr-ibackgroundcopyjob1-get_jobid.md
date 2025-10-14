---
UID: NF:qmgr.IBackgroundCopyJob1.get_JobID
title: IBackgroundCopyJob1::get_JobID (qmgr.h)
description: Use the get_JobID method to retrieve the job's identifier.
helpviewer_keywords: ["IBackgroundCopyJob1 interface [BITS]","get_JobID method","IBackgroundCopyJob1.get_JobID","IBackgroundCopyJob1::get_JobID","bits.ibackgroundcopyjob1_get_jobid","get_JobID","get_JobID method [BITS]","get_JobID method [BITS]","IBackgroundCopyJob1 interface","qmgr/IBackgroundCopyJob1::get_JobID"]
old-location: bits\ibackgroundcopyjob1_get_jobid.htm
tech.root: Bits
ms.assetid: 4f639576-33fd-413c-a163-764c0aa2ce81
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyJob1 interface [BITS],get_JobID method, IBackgroundCopyJob1.get_JobID, IBackgroundCopyJob1::get_JobID, bits.ibackgroundcopyjob1_get_jobid, get_JobID, get_JobID method [BITS], get_JobID method [BITS],IBackgroundCopyJob1 interface, qmgr/IBackgroundCopyJob1::get_JobID
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
 - IBackgroundCopyJob1::get_JobID
 - qmgr/IBackgroundCopyJob1::get_JobID
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
 - IBackgroundCopyJob1.get_JobID
---

# IBackgroundCopyJob1::get_JobID


## -description

<p class="CCE_Message">[<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Use the <b>get_JobID</b> method to retrieve the job's identifier.

## -parameters

### -param pguidJobID [out]

GUID that uniquely identifies the job.

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
Successfully retrieved the GUID that identifies the job.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopyjob1">IBackgroundCopyJob1</a>