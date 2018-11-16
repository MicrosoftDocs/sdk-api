---
UID: NF:vswriter.CVssWriterEx2.GetSessionId
title: CVssWriterEx2::GetSessionId
author: windows-sdk-content
description: Returns the writer's session identifier.
old-location: base\cvsswriterex2_getsessionid.htm
tech.root: VSS
ms.assetid: bea5ba9c-538b-453f-ae6d-12b94b8edeb6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CVssWriterEx2 interface,GetSessionId method, CVssWriterEx2.GetSessionId, CVssWriterEx2::GetSessionId, GetSessionId, GetSessionId method, GetSessionId method,CVssWriterEx2 interface, base.cvsswriterex2_getsessionid, vswriter/CVssWriterEx2::GetSessionId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- CVssWriterEx2.GetSessionId
: 
---

# CVssWriterEx2::GetSessionId


## -description


Returns the writer's session identifier.


## -parameters




### -param idSession [out]

A pointer to a variable that receives the session identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The session identifier is an opaque value that uniquely identifies a backup or restore session. It is used to distinguish the current session among multiple parallel backup or restore sessions.

As a best practice, writers and requesters should include the session ID in all diagnostics messages used for event logging and tracing.

If a writer's event handler (such as <a href="https://msdn.microsoft.com/2aff5e87-4053-46a0-a7fb-7411e76166ba">CVssWriter::OnFreeze</a>) calls this method, it must do so in the same thread that called the event handler. For more information, see 
<a href="writers.htm">Writer Event Handling</a>.




## -see-also




<a href="https://msdn.microsoft.com/13cdeae3-dece-42ae-8bff-037ee3e4cec4">CVssWriterEx2</a>



<a href="https://msdn.microsoft.com/ad7e548a-9f7a-4e35-9811-edb68458a1df">IVssBackupComponentsEx3::GetSessionId</a>
 

 

