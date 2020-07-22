---
UID: NL:vsbackup.IVssBackupComponentsEx3
title: IVssBackupComponentsEx3 (vsbackup.h)
description: Defines additional methods that requesters can use to perform LUN resynchronization and return extended writer status information.
helpviewer_keywords: ["IVssBackupComponentsEx3","IVssBackupComponentsEx3 interface","IVssBackupComponentsEx3 interface","described","base.ivssbackupcomponentsex3","vsbackup/IVssBackupComponentsEx3"]
old-location: base\ivssbackupcomponentsex3.htm
tech.root: base
ms.assetid: 56c8e7c2-2d94-4674-bd20-bf036991474f
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx3, IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,described, base.ivssbackupcomponentsex3, vsbackup/IVssBackupComponentsEx3
f1_keywords:
- vsbackup/IVssBackupComponentsEx3
dev_langs:
- c++
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- IVssBackupComponentsEx3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponentsEx3 class


## -description


Defines additional methods that 
    requesters can use to perform LUN resynchronization and return extended writer status information.

To obtain an instance of the <b>IVssBackupComponentsEx3</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx3</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>. <b>IVssBackupComponentsEx3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssBackupComponentsEx3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-addsnapshottorecoveryset">AddSnapshotToRecoverySet</a>
</td>
<td align="left" width="63%">
Specifies the volumes to be included in a LUN resynchronization operation. This method is supported only on Windows server operating systems.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-getsessionid">GetSessionId</a>
</td>
<td align="left" width="63%">
Returns the requester's session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex">GetWriterStatusEx</a>
</td>
<td align="left" width="63%">
Returns extended status information for the specified writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-recoverset">RecoverSet</a>
</td>
<td align="left" width="63%">
Initiates a LUN resynchronization operation. This method is supported only on Windows server operating systems.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex2">IVssBackupComponentsEx2</a>
 

 

