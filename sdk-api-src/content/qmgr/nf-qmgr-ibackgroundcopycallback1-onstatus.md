---
UID: NF:qmgr.IBackgroundCopyCallback1.OnStatus
title: IBackgroundCopyCallback1::OnStatus (qmgr.h)
description: Implement the OnStatus method to receive notification when the group is complete or an error occurs.
helpviewer_keywords: ["IBackgroundCopyCallback1 interface [BITS]","OnStatus method","IBackgroundCopyCallback1.OnStatus","IBackgroundCopyCallback1::OnStatus","OnStatus","OnStatus method [BITS]","OnStatus method [BITS]","IBackgroundCopyCallback1 interface","bits.ibackgroundcopycallback1_onstatus","qmgr/IBackgroundCopyCallback1::OnStatus"]
old-location: bits\ibackgroundcopycallback1_onstatus.htm
tech.root: Bits
ms.assetid: 88f75a65-8d27-4413-8b00-4caf11fbcc5e
ms.date: 12/05/2018
ms.keywords: IBackgroundCopyCallback1 interface [BITS],OnStatus method, IBackgroundCopyCallback1.OnStatus, IBackgroundCopyCallback1::OnStatus, OnStatus, OnStatus method [BITS], OnStatus method [BITS],IBackgroundCopyCallback1 interface, bits.ibackgroundcopycallback1_onstatus, qmgr/IBackgroundCopyCallback1::OnStatus
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyCallback1::OnStatus
 - qmgr/IBackgroundCopyCallback1::OnStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qmgr.h
api_name:
 - IBackgroundCopyCallback1.OnStatus
---

# IBackgroundCopyCallback1::OnStatus


## -description

<p class="CCE_Message">[<b>IBackgroundCopyCallback1</b> is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/desktop/Bits/bits-interfaces">BITS interfaces</a>.]

Implement the <b>OnStatus</b> method to receive notification when the group is complete or an error occurs.

## -parameters

### -param pGroup [in]

Interface pointer to the group that generated the event.

### -param pJob [in]

Interface pointer to the job associated with the event or <b>NULL</b> if the event is not associated with a job.

### -param dwFileIndex [in]

Index to the file associated with the error or -1. To retrieve the file, call the <a href="/windows/desktop/api/qmgr/nf-qmgr-ibackgroundcopyjob1-getfile">IBackgroundCopyJob1::GetFile</a> method.

### -param dwStatus [in]

The state of the group. The state of the group is either complete (all jobs in the group have been downloaded) or in error. An error occurred if the QM_STATUS_GROUP_ERROR flag is set. Otherwise, the group is complete.

### -param dwNumOfRetries [in]

Number of times QMGR tried to download the group after an error occurs. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.

### -param dwWin32Result [in]

Win32 error code. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.

### -param dwTransportResult [in]

HTTP error code. Valid only if the QM_STATUS_GROUP_ERROR <i>dwStatus</i> flag is set.

## -returns

This method should return <b>S_OK</b>; otherwise, the service continues to call this method until S_OK is returned. The interval at which the implementation is called is arbitrary.

## -see-also

<a href="/windows/desktop/api/qmgr/nn-qmgr-ibackgroundcopycallback1">IBackgroundCopyCallback1</a>