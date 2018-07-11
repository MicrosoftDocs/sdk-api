---
UID: NF:vswriter.CVssWriter.GetCurrentSnapshotSetId
title: CVssWriter::GetCurrentSnapshotSetId
author: windows-sdk-content
description: The GetCurrentSnapshotSetId method returns the unique identifier of the shadow copy set.
old-location: base\cvsswriter_getcurrentsnapshotsetid.htm
old-project: vss
ms.assetid: c9327bfc-02e5-402c-b445-15eed4433176
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CVssWriter interface [VSS],GetCurrentSnapshotSetId method, CVssWriter.GetCurrentSnapshotSetId, CVssWriter::GetCurrentSnapshotSetId, GetCurrentSnapshotSetId, GetCurrentSnapshotSetId method [VSS], GetCurrentSnapshotSetId method [VSS],CVssWriter interface, _win32_cvsswriter_getcurrentsnapshotsetid, base.cvsswriter_getcurrentsnapshotsetid, vswriter/CVssWriter::GetCurrentSnapshotSetId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::GetCurrentSnapshotSetId


## -description


The 
<b>GetCurrentSnapshotSetId</b> method returns the unique identifier of the shadow copy set.

<b>GetCurrentSnapshotSetId</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns the 
<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> value of the current shadow copy set.

The shadow copy set ID returned by <b>GetCurrentSnapshotSetId</b> is the shadow copy set ID of the backup operation a writer is currently participating in.

Note that a writer could be involved in more than one backup operation at a given time. Therefore, if this method is not called as part of a backup sequence—that is, not called from an event handler—which shadow copy set ID is returned is unpredictable.

If <b>GetCurrentSnapshotSetId</b> is called as part of a backup sequence—for example, from within 
<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>, <a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>, or <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>—the VSS infrastructure guarantees that the <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> value returned is that of the shadow copy supporting the current backup operation.

However, this cannot be said for calls to <b>GetCurrentSnapshotSetId</b> from within the 
<a href="vssgloss_b.htm">BackupShutdown</a> event handler 
<a href="https://msdn.microsoft.com/4b6d5efe-703b-4245-81d8-e2fc7f650d4b">CVssWriter::OnBackupShutdown</a>. If a <i>BackupShutdown</i> event is called because of an abrupt shutdown of a requester, the <a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> returned could be that of another backup operation the writer was participating in.

<b>GetCurrentSnapshotSetId</b> cannot be called after <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a> returns.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/36028e9f-f7a7-41f1-a570-48f943e9ab83">CVssWriter::OnThaw</a>



<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a>
 

 

