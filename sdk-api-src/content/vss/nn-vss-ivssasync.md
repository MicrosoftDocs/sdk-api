---
UID: NN:vss.IVssAsync
title: IVssAsync (vss.h)
description: The IVssAsync interface is returned to calling applications by methods that initiate asynchronous operations, which run in the background and typically require a long time to complete.
helpviewer_keywords: ["IVssAsync","IVssAsync interface [VSS]","IVssAsync interface [VSS]","described","_win32_ivssasync","base.ivssasync","vss/IVssAsync"]
old-location: base\ivssasync.htm
tech.root: base
ms.assetid: d2cff547-b4ff-454d-8e0e-cd29b91cbb07
ms.date: 12/05/2018
ms.keywords: IVssAsync, IVssAsync interface [VSS], IVssAsync interface [VSS],described, _win32_ivssasync, base.ivssasync, vss/IVssAsync
req.header: vss.h
req.include-header: 
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
 - IVssAsync
 - vss/IVssAsync
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
 - IVssAsync
---

# IVssAsync interface


## -description

The <b>IVssAsync</b> interface is returned to calling applications 
    by methods that initiate asynchronous operations, which run in the background and typically require a long time 
    to complete.

The <b>IVssAsync</b> interface permits an application to monitor and 
    control an asynchronous operation by waiting on its completion, querying its status, or canceling it.

The calling application is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the 
    resources held by the returned <b>IVssAsync</b> interface when it is 
    no longer needed.

The following methods return an <b>IVssAsync</b> interface:
<ul>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-importsnapshots">IVssBackupComponents::ImportSnapshots</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">IVssBackupComponents::PostRestore</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>
</li>
<li>
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>
</li>
</ul>

## -inheritance

The <b>IVssAsync</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssAsync</b> also has these types of members:

