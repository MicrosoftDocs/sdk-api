---
UID: NF:vsbackup.IVssBackupComponents.FreeWriterStatus
title: IVssBackupComponents::FreeWriterStatus method
author: windows-driver-content
description: The FreeWriterStatus method frees system resources allocated during the call to IVssBackupComponents::GatherWriterStatus.
old-location: base\ivssbackupcomponents_freewriterstatus.htm
old-project: VSS
ms.assetid: 2bf4c575-f94d-43df-b141-94ed5a55294b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: FreeWriterStatus method [VSS], FreeWriterStatus method [VSS], IVssBackupComponents interface, FreeWriterStatus,IVssBackupComponents.FreeWriterStatus, IVssBackupComponents, IVssBackupComponents interface [VSS], FreeWriterStatus method, IVssBackupComponents::FreeWriterStatus, _win32_ivssbackupcomponents_freewriterstatus, base.ivssbackupcomponents_freewriterstatus, vsbackup/IVssBackupComponents::FreeWriterStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponents.FreeWriterStatus
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::FreeWriterStatus method


## -description


The 
<b>FreeWriterStatus</b> method frees system resources allocated during the call to <a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a>.


## -parameters






## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer status was successfully freed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a>
 

 

