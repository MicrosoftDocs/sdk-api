---
UID: NE:objidl.tagSERVERCALL
title: SERVERCALL (objidl.h)
description: Indicates the status of server call.
helpviewer_keywords: ["SERVERCALL","SERVERCALL enumeration [COM]","SERVERCALL_ISHANDLED","SERVERCALL_REJECTED","SERVERCALL_RETRYLATER","_com_SERVERCALL","com.servercall","objidl/SERVERCALL","objidl/SERVERCALL_ISHANDLED","objidl/SERVERCALL_REJECTED","objidl/SERVERCALL_RETRYLATER"]
old-location: com\servercall.htm
tech.root: com
ms.assetid: 2a9b5e85-44b9-43c1-b3e5-a8f2c140b674
ms.date: 12/05/2018
ms.keywords: SERVERCALL, SERVERCALL enumeration [COM], SERVERCALL_ISHANDLED, SERVERCALL_REJECTED, SERVERCALL_RETRYLATER, _com_SERVERCALL, com.servercall, objidl/SERVERCALL, objidl/SERVERCALL_ISHANDLED, objidl/SERVERCALL_REJECTED, objidl/SERVERCALL_RETRYLATER
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SERVERCALL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSERVERCALL
 - objidl/tagSERVERCALL
 - SERVERCALL
 - objidl/SERVERCALL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - SERVERCALL
---

# SERVERCALL enumeration


## -description

Indicates the status of server call.

## -enum-fields

### -field SERVERCALL_ISHANDLED:0

The object may be able to process the call.

### -field SERVERCALL_REJECTED:1

The object cannot handle the call due to an unforeseen problem, such as network unavailability.

### -field SERVERCALL_RETRYLATER:2

The object cannot handle the call at this time. For example, an application might return this value when it is in a user-controlled modal state.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-handleincomingcall">IMessageFilter::HandleInComingCall</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imessagefilter-retryrejectedcall">IMessageFilter::RetryRejectedCall</a>
