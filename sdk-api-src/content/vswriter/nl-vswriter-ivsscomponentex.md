---
UID: NL:vswriter.IVssComponentEx
title: IVssComponentEx (vswriter.h)
description: Defines additional methods for examining and modifying information about components contained in a requester's Backup Components Document.
old-location: base\ivsscomponentex.htm
tech.root: VSS
ms.assetid: b11f65b0-2de2-478b-88b6-4696a8da2419
ms.date: 12/05/2018
ms.keywords: IVssComponentEx, IVssComponentEx interface, IVssComponentEx interface,described, base.ivsscomponentex, vswriter/IVssComponentEx
f1_keywords:
- vswriter/IVssComponentEx
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
- IVssComponentEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssComponentEx class


## -description


Defines additional methods for examining  and modifying information about components contained in a requester's Backup 
    Components Document.

The <b>IVssComponentEx</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssComponentEx</b> 
   interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of the 
   <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> interface, and pass 
   the <b>IID_IVssComponentEx</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponentEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>. <b>IVssComponentEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssComponentEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getauthoritativerestore">GetAuthoritativeRestore</a>
</td>
<td align="left" width="63%">
Determines whether a requester has marked the restore of a component as authoritative for a replicated data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg">GetPostSnapshotFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> failure message string that a writer has  set for a given component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg">GetPrepareForBackupFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> failure message string that a writer has  set for a given component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getrestorename">GetRestoreName</a>
</td>
<td align="left" width="63%">
Obtains the logical name assigned to a component that is being restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-getrollforward">GetRollForward</a>
</td>
<td align="left" width="63%">
Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg">SetPostSnapshotFailureMsg</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> failure message string for a component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg">SetPrepareForBackupFailureMsg</a>
</td>
<td align="left" width="63%">
Sets a <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-p">PrepareForBackup</a> failure message string for a component.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>
 

 

