---
UID: NS:sspi._SecPkgContext_NamesA
title: "_SecPkgContext_NamesA"
author: windows-sdk-content
description: The SecPkgContext_Names structure indicates the name of the user associated with a security context. The QueryContextAttributes (General) function uses this structure.
old-location: security\secpkgcontext_names.htm
tech.root: secauthn
ms.assetid: 9df0bf7c-ad5f-4cb8-8934-76062789735f
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PSecPkgContext_NamesA, SecPkgContext_Names, SecPkgContext_Names structure [Security], SecPkgContext_NamesA, SecPkgContext_NamesW, _SecPkgContext_NamesA, _ssp_secpkgcontext_names, pSecPkgContext_Names, pSecPkgContext_Names structure pointer [Security], security.secpkgcontext_names, sspi/SecPkgContext_Names, sspi/SecPkgContext_NamesA, sspi/SecPkgContext_NamesW, sspi/pSecPkgContext_Names"
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
req.unicode-ansi: SecPkgContext_NamesW (Unicode) and SecPkgContext_NamesA (ANSI)
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
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_Names
 - SecPkgContext_NamesA
 - SecPkgContext_NamesW
product: Windows
targetos: Windows
req.typenames: SecPkgContext_NamesA, *PSecPkgContext_NamesA
req.redist: 
---

# _SecPkgContext_NamesA structure


## -description


The <b>SecPkgContext_Names</b> structure indicates the name of the user associated with a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function uses this structure.


## -struct-fields




### -field sUserName

Pointer to a null-terminated string containing the name of the user represented by the context. If the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> has set the SECPKG_FLAG_ACCEPT_WIN32_NAME flag, this name can be used in other Windows calls.


## -see-also




<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>
 

 

