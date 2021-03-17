---
UID: NS:ntsecapi._PKU2U_CREDUI_CONTEXT
title: PKU2U_CREDUI_CONTEXT (ntsecapi.h)
description: Specifies a PKU2U client context.
helpviewer_keywords: ["*PPKU2U_CREDUI_CONTEXT","PKU2U_CREDUI_CONTEXT","PKU2U_CREDUI_CONTEXT structure [Security]","PPKU2U_CREDUI_CONTEXT","PPKU2U_CREDUI_CONTEXT structure pointer [Security]","ntsecapi/PKU2U_CREDUI_CONTEXT","ntsecapi/PPKU2U_CREDUI_CONTEXT","security.pku2u_credui_context"]
old-location: security\pku2u_credui_context.htm
tech.root: security
ms.assetid: 38de5472-27f2-40d4-90e8-7b59d3982f03
ms.date: 12/05/2018
ms.keywords: '*PPKU2U_CREDUI_CONTEXT, PKU2U_CREDUI_CONTEXT, PKU2U_CREDUI_CONTEXT structure [Security], PPKU2U_CREDUI_CONTEXT, PPKU2U_CREDUI_CONTEXT structure pointer [Security], ntsecapi/PKU2U_CREDUI_CONTEXT, ntsecapi/PPKU2U_CREDUI_CONTEXT, security.pku2u_credui_context'
req.header: ntsecapi.h
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
req.typenames: PKU2U_CREDUI_CONTEXT, *PPKU2U_CREDUI_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PKU2U_CREDUI_CONTEXT
 - ntsecapi/_PKU2U_CREDUI_CONTEXT
 - PPKU2U_CREDUI_CONTEXT
 - ntsecapi/PPKU2U_CREDUI_CONTEXT
 - PKU2U_CREDUI_CONTEXT
 - ntsecapi/PKU2U_CREDUI_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - PKU2U_CREDUI_CONTEXT
---

# PKU2U_CREDUI_CONTEXT structure


## -description

Specifies a PKU2U client context.

## -struct-fields

### -field Version

The version number of the context. This must be <b>PKU2U_CREDUI_CONTEXT_VERSION</b>.

### -field cbHeaderLength

The size, in bytes, of this structure, not including the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-pku2u_cert_blob">PKU2U_CERT_BLOB</a> structure that follows it.

### -field cbStructureLength

The size, in bytes, of this structure, including the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-pku2u_cert_blob">PKU2U_CERT_BLOB</a> structure that follows it.

### -field CertArrayCount

The size, in bytes, of the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-pku2u_cert_blob">PKU2U_CERT_BLOB</a> structure that follows this structure.

### -field CertArrayOffset

The number of bytes from the beginning of this structure in memory to the beginning of the <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-pku2u_cert_blob">PKU2U_CERT_BLOB</a> structure that follows this structure.