---
UID: NS:sspi._SecPkgContext_Flags
title: "_SecPkgContext_Flags"
author: windows-sdk-content
description: The SecPkgContext_Flags structure contains information about the flags in the current security context. This structure is returned by QueryContextAttributes (General).
old-location: security\secpkgcontext_flags.htm
old-project: SecAuthN
ms.assetid: 0be0e945-4048-4748-a9fd-15d08fb7ff3e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PSecPkgContext_Flags, PSecPkgContext_Flags, PSecPkgContext_Flags structure pointer [Security], SecPkgContext_Flags, SecPkgContext_Flags structure [Security], _SecPkgContext_Flags, security.secpkgcontext_flags, sspi/PSecPkgContext_Flags, sspi/SecPkgContext_Flags"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
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
req.typenames: SecPkgContext_Flags, *PSecPkgContext_Flags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_Flags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_Flags structure


## -description


The <b>SecPkgContext_Flags</b> structure contains information about the flags in the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. This structure is returned by <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>.


## -struct-fields




### -field Flags

Flag values for the current security context. These values correspond to the flags negotiated by the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> and <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> functions.

