---
UID: NL:vsbackup.IVssBackupComponentsEx2
title: IVssBackupComponentsEx2
author: windows-sdk-content
description: Defines additional methods that requesters can use to run backup and restore operations.
old-location: base\ivssbackupcomponentsex2.htm
old-project: VSS
ms.assetid: 69d4d500-0e21-48bd-b90b-d06c88fde136
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssBackupComponentsEx2, IVssBackupComponentsEx2 interface, IVssBackupComponentsEx2 interface,described, base.ivssbackupcomponentsex2, vsbackup/IVssBackupComponentsEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
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
req.lib: VssApi.lib
req.dll: VssApi.dll
req.irql: 
req.product: Windows UI
---

# IVssBackupComponentsEx2 class


## -description


Defines additional methods that 
    requesters can use to run backup and restore operations.

To obtain an instance of the <b>IVssBackupComponentsEx2</b> 
   interface, call the <a href="https://msdn.microsoft.com/library/Dd757101(v=VS.85).aspx">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx2</b> interface inherits from <a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a> and <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>. <b>IVssBackupComponentsEx2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/595fe295-082d-4130-9698-952df49a922e">BreakSnapshotSetEx</a>
</td>
<td align="left" width="63%">
Breaks a shadow copy set according to requester-specified options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e64cb785-9688-4aba-8017-65a8494ddb33">FastRecovery</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba06e324-0f17-4184-bc53-dcb82fb49292">PreFastRecovery</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3725a282-2df8-4a0a-a1bf-a73c2b259cbf">SetAuthoritativeRestore</a>
</td>
<td align="left" width="63%">
Marks the restore of a component as authoritative for a replicated data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">SetRestoreName</a>
</td>
<td align="left" width="63%">
Assigns a new logical name to a component that is being restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">SetRollForward</a>
</td>
<td align="left" width="63%">
Sets the roll-forward operation type for a component and specifies the restore point for a partial roll-forward operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6946b65-b142-41b9-88c0-a1b11caba08e">UnexposeSnapshot</a>
</td>
<td align="left" width="63%">
Unexposes a shadow copy either by deleting the file share or by removing the drive letter or mounted folder.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a>
 

 

