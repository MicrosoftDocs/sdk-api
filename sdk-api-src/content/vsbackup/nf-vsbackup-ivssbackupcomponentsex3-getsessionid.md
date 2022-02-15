---
UID: NF:vsbackup.IVssBackupComponentsEx3.GetSessionId
title: IVssBackupComponentsEx3::GetSessionId (vsbackup.h)
description: Returns the requester's session identifier.
helpviewer_keywords: ["GetSessionId","GetSessionId method","GetSessionId method","IVssBackupComponentsEx3 interface","IVssBackupComponentsEx3 interface","GetSessionId method","IVssBackupComponentsEx3.GetSessionId","IVssBackupComponentsEx3::GetSessionId","base.ivssbackupcomponentsex3_getsessionid","vsbackup/IVssBackupComponentsEx3::GetSessionId"]
old-location: base\ivssbackupcomponentsex3_getsessionid.htm
tech.root: base
ms.assetid: ad7e548a-9f7a-4e35-9811-edb68458a1df
ms.date: 12/05/2018
ms.keywords: GetSessionId, GetSessionId method, GetSessionId method,IVssBackupComponentsEx3 interface, IVssBackupComponentsEx3 interface,GetSessionId method, IVssBackupComponentsEx3.GetSessionId, IVssBackupComponentsEx3::GetSessionId, base.ivssbackupcomponentsex3_getsessionid, vsbackup/IVssBackupComponentsEx3::GetSessionId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponentsEx3::GetSessionId
 - vsbackup/IVssBackupComponentsEx3::GetSessionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsBackup.h
api_name:
 - IVssBackupComponentsEx3.GetSessionId
---

# IVssBackupComponentsEx3::GetSessionId


## -description

Returns the requester's session identifier.

## -parameters

### -param idSession [out]

A pointer to a variable that receives the session identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The session identifier is an opaque value that uniquely identifies a backup or restore session. It is used to distinguish the current session among multiple parallel backup or restore sessions.

As a best practice, writers and requesters should include the session ID in all diagnostics messages used for event logging and tracing.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex2-getsessionid">CVssWriterEx2::GetSessionId</a>



<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex3">IVssBackupComponentsEx3</a>