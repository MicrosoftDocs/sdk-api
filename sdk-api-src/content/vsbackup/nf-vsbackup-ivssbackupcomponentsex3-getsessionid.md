---
UID: NF:vsbackup.IVssBackupComponentsEx3.GetSessionId
title: IVssBackupComponentsEx3::GetSessionId (vsbackup.h)
author: windows-sdk-content
description: Returns the requester's session identifier.
old-location: base\ivssbackupcomponentsex3_getsessionid.htm
tech.root: VSS
ms.assetid: ad7e548a-9f7a-4e35-9811-edb68458a1df
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSessionId, GetSessionId method, GetSessionId method,IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,GetSessionId method, IVssBackupComponentsEx3.GetSessionId, IVssBackupComponentsEx3::GetSessionId, base.ivssbackupcomponentsex3_getsessionid, vsbackup/IVssBackupComponentsEx3::GetSessionId
ms.topic: method
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
 - IVssBackupComponentsEx3.GetSessionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponentsEx3::GetSessionId


## -description


Returns the requester's session identifier.


## -parameters




### -param idSession [out]

A pointer to a variable that receives the session identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The session identifier is an opaque value that uniquely identifies a backup or restore session. It is used to distinguish the current session among multiple parallel backup or restore sessions.

As a best practice, writers and requesters should include the session ID in all diagnostics messages used for event logging and tracing.




## -see-also




<a href="https://msdn.microsoft.com/bea5ba9c-538b-453f-ae6d-12b94b8edeb6">CVssWriterEx2::GetSessionId</a>



<a href="https://msdn.microsoft.com/56c8e7c2-2d94-4674-bd20-bf036991474f">IVssBackupComponentsEx3</a>
 

 

