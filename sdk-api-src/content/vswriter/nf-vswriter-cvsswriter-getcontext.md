---
UID: NF:vswriter.CVssWriter.GetContext
title: CVssWriter::GetContext (vswriter.h)
description: The GetContext information returns the current context for any ongoing or possible shadow copies.
helpviewer_keywords: ["CVssWriter interface [VSS]","GetContext method","CVssWriter.GetContext","CVssWriter::GetContext","GetContext","GetContext method [VSS]","GetContext method [VSS]","CVssWriter interface","_win32_cvsswriter_getcontext","base.cvsswriter_getcontext","vswriter/CVssWriter::GetContext"]
old-location: base\cvsswriter_getcontext.htm
tech.root: base
ms.assetid: efe2f43b-fbcf-4b30-a6d4-31d563d321c5
ms.date: 12/05/2018
ms.keywords: CVssWriter interface [VSS],GetContext method, CVssWriter.GetContext, CVssWriter::GetContext, GetContext, GetContext method [VSS], GetContext method [VSS],CVssWriter interface, _win32_cvsswriter_getcontext, base.cvsswriter_getcontext, vswriter/CVssWriter::GetContext
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - CVssWriter::GetContext
 - vswriter/CVssWriter::GetContext
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
 - CVssWriter.GetContext
---

# CVssWriter::GetContext


## -description

The 
<b>GetContext</b> information returns the current context for any ongoing or possible shadow copies.

<b>GetContext</b> is a protected method implemented by the 
<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class.



## -returns

This method returns the context for any shadow copies involving the writer as a bit mask (or bitwise OR) of 
<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a> and 
<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values.

## -remarks

The default context for a shadow copy is VSS_CTX_BACKUP.

A requester can set the context for a shadow copy by calling 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a> at any time prior to creating a shadow copy with 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>.


<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> generates a number of events (<a href="/windows/desktop/VSS/vssgloss-p">PrepareForSnapshot</a>, <a href="/windows/desktop/VSS/vssgloss-f">Freeze</a>, <a href="/windows/desktop/VSS/vssgloss-t">Thaw</a>, <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a>), the first of which is <i>PrepareForSnapshot</i>.

Therefore, if a writer is participating in a shadow copy operation, a definitive value of that shadow copy's context cannot be found when 
<b>GetContext</b> is called prior to 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparesnapshot">CVssWriter::OnPrepareSnapshot</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">IVssBackupComponents::SetContext</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_snapshot_context">_VSS_SNAPSHOT_CONTEXT</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
