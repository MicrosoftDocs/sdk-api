---
UID: NS:sspi._SecPkgContext_TargetInformation
title: "_SecPkgContext_TargetInformation"
author: windows-sdk-content
description: Returns information about the credential used for the security context.
old-location: security\secpkgcontext_targetinformation.htm
old-project: SecAuthN
ms.assetid: 8a5a6bd6-8678-4544-a631-5ee4347bc685
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSecPkgContext_TargetInformation, PSecPkgContext_TargetInformation, PSecPkgContext_TargetInformation structure pointer [Security], SecPkgContext_TargetInformation, SecPkgContext_TargetInformation structure [Security], _SecPkgContext_TargetInformation, security.secpkgcontext_targetinformation, sspi/PSecPkgContext_TargetInformation, sspi/SecPkgContext_TargetInformation"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: sspi.h
req.include-header: Security.h
req.redist: 
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
req.typenames: SecPkgContext_TargetInformation, *PSecPkgContext_TargetInformation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_TargetInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_TargetInformation structure


## -description


The <b>SecPkgContext_TargetInformation</b> structure returns information about the credential used for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.  This structure is returned by the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


## -struct-fields




### -field MarshalledTargetInfoLength

Size, in bytes, of <b>MarshalledTargetInfo</b>.


### -field MarshalledTargetInfo

Array of bytes that represent the credential, if a credential is provided by a credential manager.

