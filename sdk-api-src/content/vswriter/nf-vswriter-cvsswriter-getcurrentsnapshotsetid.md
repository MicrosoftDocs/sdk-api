---
UID: NF:vswriter.CVssWriter.GetCurrentSnapshotSetId
title: CVssWriter::GetCurrentSnapshotSetId (vswriter.h)
description: The GetCurrentSnapshotSetId method returns the unique identifier of the shadow copy set.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetCurrentSnapshotSetId method","CVssWriter.GetCurrentSnapshotSetId","CVssWriter::GetCurrentSnapshotSetId","GetCurrentSnapshotSetId","GetCurrentSnapshotSetId method [VSS]","GetCurrentSnapshotSetId method [VSS]","CVssWriter interface","_win32_cvsswriter_getcurrentsnapshotsetid","base.cvsswriter_getcurrentsnapshotsetid","vswriter/CVssWriter::GetCurrentSnapshotSetId"]
old-location: base\cvsswriter_getcurrentsnapshotsetid.htm
tech.root: base
ms.assetid: c9327bfc-02e5-402c-b445-15eed4433176
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentSnapshotSetId method, CVssWriter.GetCurrentSnapshotSetId, CVssWriter::GetCurrentSnapshotSetId, GetCurrentSnapshotSetId, GetCurrentSnapshotSetId method [VSS], GetCurrentSnapshotSetId method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentsnapshotsetid, base.cvsswriter_getcurrentsnapshotsetid, vswriter/CVssWriter::GetCurrentSnapshotSetId
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriter::GetCurrentSnapshotSetId
 - vswriter/CVssWriter::GetCurrentSnapshotSetId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriter.GetCurrentSnapshotSetId
---

# CVssWriter::GetCurrentSnapshotSetId


## -description

The 
<b>GetCurrentSnapshotSetId</b> method returns the unique identifier of the shadow copy set.

<b>GetCurrentSnapshotSetId</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns the 
<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> value of the current shadow copy set.

The shadow copy set ID returned by <b>GetCurrentSnapshotSetId</b> is the shadow copy set ID of the backup operation a writer is currently participating in.

Note that a writer could be involved in more than one backup operation at a given time. Therefore, if this method is not called as part of a backup sequence—that is, not called from an event handler—which shadow copy set ID is returned is unpredictable.

If <b>GetCurrentSnapshotSetId</b> is called as part of a backup sequence—for example, from within 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>, <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>, or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>—the VSS infrastructure guarantees that the <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> value returned is that of the shadow copy supporting the current backup operation.

However, this cannot be said for calls to <b>GetCurrentSnapshotSetId</b> from within the 
<a href="/windows/desktop/VSS/vssgloss-b">BackupShutdown</a> event handler 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupshutdown">CVssWriter::OnBackupShutdown</a>. If a <i>BackupShutdown</i> event is called because of an abrupt shutdown of a requester, the <a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> returned could be that of another backup operation the writer was participating in.

<b>GetCurrentSnapshotSetId</b> cannot be called after <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a> returns.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onthaw">CVssWriter::OnThaw</a>



<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a>
