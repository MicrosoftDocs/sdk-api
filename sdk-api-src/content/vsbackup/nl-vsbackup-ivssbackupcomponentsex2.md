---
UID: NL:vsbackup.IVssBackupComponentsEx2
title: IVssBackupComponentsEx2 (vsbackup.h)
author: windows-sdk-content
description: Defines additional methods that requesters can use to run backup and restore operations.
old-location: base\ivssbackupcomponentsex2.htm
tech.root: VSS
ms.assetid: 69d4d500-0e21-48bd-b90b-d06c88fde136
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx2, IVssBackupComponentsEx2 interface, IVssBackupComponentsEx2 interface,described, base.ivssbackupcomponentsex2, vsbackup/IVssBackupComponentsEx2
ms.topic: class
f1_keywords: 
 - "vsbackup/IVssBackupComponentsEx2"
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponentsEx2 class


## -description


Defines additional methods that 
    requesters can use to run backup and restore operations.

To obtain an instance of the <b>IVssBackupComponentsEx2</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssBackupComponentsEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex">BreakSnapshotSetEx</a>
</td>
<td align="left" width="63%">
Breaks a shadow copy set according to requester-specified options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-fastrecovery">FastRecovery</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-prefastrecovery">PreFastRecovery</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore">SetAuthoritativeRestore</a>
</td>
<td align="left" width="63%">
Marks the restore of a component as authoritative for a replicated data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename">SetRestoreName</a>
</td>
<td align="left" width="63%">
Assigns a new logical name to a component that is being restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward">SetRollForward</a>
</td>
<td align="left" width="63%">
Sets the roll-forward operation type for a component and specifies the restore point for a partial roll-forward operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot">UnexposeSnapshot</a>
</td>
<td align="left" width="63%">
Unexposes a shadow copy either by deleting the file share or by removing the drive letter or mounted folder.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>
 

 

