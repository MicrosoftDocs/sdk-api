---
UID: NN:vss.IVssAsync
title: IVssAsync (vss.h)

description: The IVssAsync interface is returned to calling applications by methods that initiate asynchronous operations, which run in the background and typically require a long time to complete.
old-location: base\ivssasync.htm
tech.root: VSS
ms.assetid: d2cff547-b4ff-454d-8e0e-cd29b91cbb07

ms.date: 12/05/2018
ms.keywords: IVssAsync, IVssAsync interface [VSS], IVssAsync interface [VSS],described, _win32_ivssasync, base.ivssasync, vss/IVssAsync
ms.topic: interface
f1_keywords: 
 - "vss/IVssAsync"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssAsync interface


## -description


The <b>IVssAsync</b> interface is returned to calling applications 
    by methods that initiate asynchronous operations, which run in the background and typically require a long time 
    to complete.

The <b>IVssAsync</b> interface permits an application to monitor and 
    control an asynchronous operation by waiting on its completion, querying its status, or canceling it.

The calling application is responsible for calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> to release the 
    resources held by the returned <b>IVssAsync</b> interface when it is 
    no longer needed.

The following methods return an <b>IVssAsync</b> interface:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">IVssBackupComponents::BackupComplete</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">IVssBackupComponents::GatherWriterStatus</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-importsnapshots">IVssBackupComponents::ImportSnapshots</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">IVssBackupComponents::PostRestore</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">IVssBackupComponents::PrepareForBackup</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">IVssBackupComponents::PreRestore</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssAsync</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssasync-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an incomplete asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">QueryStatus</a>
</td>
<td align="left" width="63%">
Queries the status of an asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vss/nf-vss-ivssasync-wait">Wait</a>
</td>
<td align="left" width="63%">
Waits until an incomplete asynchronous operation will be finished, and the operation's completion status.

</td>
</tr>
</table> 

