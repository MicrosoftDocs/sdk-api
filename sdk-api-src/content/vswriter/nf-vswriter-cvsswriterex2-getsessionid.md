---
UID: NF:vswriter.CVssWriterEx2.GetSessionId
title: CVssWriterEx2::GetSessionId (vswriter.h)
description: Returns the writer's session identifier.
helpviewer_keywords: ["CVssWriterEx2 interface","GetSessionId method","CVssWriterEx2.GetSessionId","CVssWriterEx2::GetSessionId","GetSessionId","GetSessionId method","GetSessionId method","CVssWriterEx2 interface","base.cvsswriterex2_getsessionid","vswriter/CVssWriterEx2::GetSessionId"]
old-location: base\cvsswriterex2_getsessionid.htm
tech.root: base
ms.assetid: bea5ba9c-538b-453f-ae6d-12b94b8edeb6
ms.date: 12/05/2018
ms.keywords: CVssWriterEx2 interface,GetSessionId method, CVssWriterEx2.GetSessionId, CVssWriterEx2::GetSessionId, GetSessionId, GetSessionId method, GetSessionId method,CVssWriterEx2 interface, base.cvsswriterex2_getsessionid, vswriter/CVssWriterEx2::GetSessionId
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriterEx2::GetSessionId
 - vswriter/CVssWriterEx2::GetSessionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx2.GetSessionId
---

# CVssWriterEx2::GetSessionId


## -description

Returns the writer's session identifier.

## -parameters

### -param idSession [out]

A pointer to a variable that receives the session identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The session identifier is an opaque value that uniquely identifies a backup or restore session. It is used to distinguish the current session among multiple parallel backup or restore sessions.

As a best practice, writers and requesters should include the session ID in all diagnostics messages used for event logging and tracing.

If a writer's event handler (such as <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onfreeze">CVssWriter::OnFreeze</a>) calls this method, it must do so in the same thread that called the event handler. For more information, see 
<a href="/windows/desktop/VSS/writers">Writer Event Handling</a>.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex2">CVssWriterEx2</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex3-getsessionid">IVssBackupComponentsEx3::GetSessionId</a>