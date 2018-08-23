---
UID: NF:vswriter.CVssWriter.GetContext
title: CVssWriter::GetContext
author: windows-sdk-content
description: The GetContext information returns the current context for any ongoing or possible shadow copies.
old-location: base\cvsswriter_getcontext.htm
old-project: vss
ms.assetid: efe2f43b-fbcf-4b30-a6d4-31d563d321c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CVssWriter interface [VSS],GetContext method, CVssWriter.GetContext, CVssWriter::GetContext, GetContext, GetContext method [VSS], GetContext method [VSS],CVssWriter interface, _win32_cvsswriter_getcontext, base.cvsswriter_getcontext, vswriter/CVssWriter::GetContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.redist: 
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
 - CVssWriter.GetContext
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::GetContext


## -description


The 
<b>GetContext</b> information returns the current context for any ongoing or possible shadow copies.

<b>GetContext</b> is a protected method implemented by the 
<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class.


## -parameters






## -returns



This method returns the context for any shadow copies involving the writer as a bit mask (or bitwise OR) of 
<a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a> and 
<a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> values.




## -remarks



The default context for a shadow copy is VSS_CTX_BACKUP.

A requester can set the context for a shadow copy by calling 
<a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">IVssBackupComponents::SetContext</a> at any time prior to creating a shadow copy with 
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>.


<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a> generates a number of events (<a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForSnapshot</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa384656(v=VS.85).aspx">Freeze</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa384668(v=VS.85).aspx">Thaw</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a>), the first of which is <i>PrepareForSnapshot</i>.

Therefore, if a writer is participating in a shadow copy operation, a definitive value of that shadow copy's context cannot be found when 
<b>GetContext</b> is called prior to 
<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/a077323e-d04c-4bf7-8aa6-5028fa1c6e6b">CVssWriter::OnPrepareSnapshot</a>



<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>



<a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">IVssBackupComponents::SetContext</a>



<a href="https://msdn.microsoft.com/2efe3066-4b91-4501-bacb-4211b222e0c3">_VSS_SNAPSHOT_CONTEXT</a>



<a href="https://msdn.microsoft.com/0326a81e-036c-4548-9e09-29054e51fadd">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>
 

 

