---
UID: NS:sspi._SEC_WINNT_CREDUI_CONTEXT_VECTOR
title: SEC_WINNT_CREDUI_CONTEXT_VECTOR (sspi.h)
description: Specifies the offset and size of the credential context data in a SEC_WINNT_CREDUI_CONTEXT structure.
helpviewer_keywords: ["*PSEC_WINNT_CREDUI_CONTEXT_VECTOR","PSEC_WINNT_CREDUI_CONTEXT_VECTOR","PSEC_WINNT_CREDUI_CONTEXT_VECTOR structure pointer [Security]","SEC_WINNT_CREDUI_CONTEXT_VECTOR","SEC_WINNT_CREDUI_CONTEXT_VECTOR structure [Security]","security.sec_winnt_credui_context_vector","sspi/PSEC_WINNT_CREDUI_CONTEXT_VECTOR","sspi/SEC_WINNT_CREDUI_CONTEXT_VECTOR"]
old-location: security\sec_winnt_credui_context_vector.htm
tech.root: security
ms.assetid: 11a82e82-f5c5-4549-8e5f-9d479e9c8249
ms.date: 12/05/2018
ms.keywords: '*PSEC_WINNT_CREDUI_CONTEXT_VECTOR, PSEC_WINNT_CREDUI_CONTEXT_VECTOR, PSEC_WINNT_CREDUI_CONTEXT_VECTOR structure pointer [Security], SEC_WINNT_CREDUI_CONTEXT_VECTOR, SEC_WINNT_CREDUI_CONTEXT_VECTOR structure [Security], security.sec_winnt_credui_context_vector, sspi/PSEC_WINNT_CREDUI_CONTEXT_VECTOR, sspi/SEC_WINNT_CREDUI_CONTEXT_VECTOR'
req.header: sspi.h
req.include-header: 
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
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SEC_WINNT_CREDUI_CONTEXT_VECTOR
 - sspi/_SEC_WINNT_CREDUI_CONTEXT_VECTOR
 - PSEC_WINNT_CREDUI_CONTEXT_VECTOR
 - sspi/PSEC_WINNT_CREDUI_CONTEXT_VECTOR
 - SEC_WINNT_CREDUI_CONTEXT_VECTOR
 - sspi/SEC_WINNT_CREDUI_CONTEXT_VECTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SEC_WINNT_CREDUI_CONTEXT_VECTOR
---

# SEC_WINNT_CREDUI_CONTEXT_VECTOR structure


## -description

Specifies the offset and size of the credential context data in a <a href="/windows/desktop/api/sspi/ns-sspi-sec_winnt_credui_context">SEC_WINNT_CREDUI_CONTEXT</a> structure.

## -struct-fields

### -field CredUIContextArrayOffset

The number of bytes from the  beginning of the structure to the context data.

### -field CredUIContextCount

The size, in bytes, of the context data.