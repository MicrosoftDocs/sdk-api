---
UID: NL:vsbackup.IVssBackupComponentsEx3
title: IVssBackupComponentsEx3 (vsbackup.h)
author: windows-sdk-content
description: Defines additional methods that requesters can use to perform LUN resynchronization and return extended writer status information.
old-location: base\ivssbackupcomponentsex3.htm
tech.root: VSS
ms.assetid: 56c8e7c2-2d94-4674-bd20-bf036991474f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssBackupComponentsEx3, IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,described, base.ivssbackupcomponentsex3, vsbackup/IVssBackupComponentsEx3
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponentsEx3 class


## -description


Defines additional methods that 
    requesters can use to perform LUN resynchronization and return extended writer status information.

To obtain an instance of the <b>IVssBackupComponentsEx3</b> 
   interface, call the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a> interface, and pass 
   the <b>IID_IVssBackupComponentsEx3</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponentsEx3</b> interface inherits from <a href="https://msdn.microsoft.com/69d4d500-0e21-48bd-b90b-d06c88fde136">IVssBackupComponentsEx2</a>, <a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a>, and <a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>. <b>IVssBackupComponentsEx3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f489d353-7c8a-45d2-8917-82d29fbdf5f5">AddSnapshotToRecoverySet</a>
</td>
<td align="left" width="63%">
Specifies the volumes to be included in a LUN resynchronization operation. This method is supported only on Windows server operating systems.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad7e548a-9f7a-4e35-9811-edb68458a1df">GetSessionId</a>
</td>
<td align="left" width="63%">
Returns the requester's session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab2be2c0-04bb-4a56-a636-ebd2c06e844a">GetWriterStatusEx</a>
</td>
<td align="left" width="63%">
Returns extended status information for the specified writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e468527-11e7-42d8-808b-2cb2eb86e0ba">RecoverSet</a>
</td>
<td align="left" width="63%">
Initiates a LUN resynchronization operation. This method is supported only on Windows server operating systems.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/d3a265ab-39cc-4861-9191-9ecf094d8826">IVssBackupComponentsEx</a>



<a href="https://msdn.microsoft.com/69d4d500-0e21-48bd-b90b-d06c88fde136">IVssBackupComponentsEx2</a>
 

 

