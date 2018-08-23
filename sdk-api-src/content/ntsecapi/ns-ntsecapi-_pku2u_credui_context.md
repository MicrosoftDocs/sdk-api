---
UID: NS:ntsecapi._PKU2U_CREDUI_CONTEXT
title: "_PKU2U_CREDUI_CONTEXT"
author: windows-sdk-content
description: Specifies a PKU2U client context.
old-location: security\pku2u_credui_context.htm
old-project: secauthn
ms.assetid: 38de5472-27f2-40d4-90e8-7b59d3982f03
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PPKU2U_CREDUI_CONTEXT, PKU2U_CREDUI_CONTEXT, PKU2U_CREDUI_CONTEXT structure [Security], PPKU2U_CREDUI_CONTEXT, PPKU2U_CREDUI_CONTEXT structure pointer [Security], _PKU2U_CREDUI_CONTEXT, ntsecapi/PKU2U_CREDUI_CONTEXT, ntsecapi/PPKU2U_CREDUI_CONTEXT, security.pku2u_credui_context"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PKU2U_CREDUI_CONTEXT, *PPKU2U_CREDUI_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - PKU2U_CREDUI_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PKU2U_CREDUI_CONTEXT structure


## -description


Specifies a PKU2U client context.


## -struct-fields




### -field Version

The version number of the context. This must be <b>PKU2U_CREDUI_CONTEXT_VERSION</b>.


### -field cbHeaderLength

The size, in bytes, of this structure, not including the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows it.


### -field cbStructureLength

The size, in bytes, of this structure, including the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows it.


### -field CertArrayCount

The size, in bytes, of the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows this structure.


### -field CertArrayOffset

The number of bytes from the beginning of this structure in memory to the beginning of the <a href="https://msdn.microsoft.com/f840e81e-3fed-4d05-8ac4-b19ce0267517">PKU2U_CERT_BLOB</a> structure that follows this structure.

