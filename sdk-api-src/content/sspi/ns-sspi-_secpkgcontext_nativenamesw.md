---
UID: NS:sspi._SecPkgContext_NativeNamesW
title: "_SecPkgContext_NativeNamesW"
author: windows-driver-content
description: The SecPkgContext_NativeNames structure returns the client and server principal names from the outbound ticket. This structure is valid only for client outbound tickets. This structure is returned by QueryContextAttributes (General).
old-location: security\secpkgcontext_nativenames.htm
old-project: SecAuthN
ms.assetid: f935093f-5661-4ced-94f1-c4b21c3b9f69
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PSecPkgContext_NativeNamesW, PSecPkgContext_NativeNames, PSecPkgContext_NativeNames structure pointer [Security], SecPkgContext_NativeNames, SecPkgContext_NativeNames structure [Security], SecPkgContext_NativeNamesW, _SecPkgContext_NativeNamesA, _SecPkgContext_NativeNamesW, security.secpkgcontext_nativenames, sspi/PSecPkgContext_NativeNames, sspi/SecPkgContext_NativeNames"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SecPkgContext_NativeNamesW, *PSecPkgContext_NativeNamesW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgContext_NativeNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_NativeNamesW structure


## -description


The <b>SecPkgContext_NativeNames</b> structure returns the client and server principal names from the outbound ticket. This structure is valid only for client outbound tickets. This structure is returned by  <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a>.


## -struct-fields




### -field sClientName

Pointer to a null-terminated string that represents the principal name for the client in the outbound ticket. This string should never be <b>NULL</b> when querying a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> negotiated with <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a>.


### -field sServerName

Pointer to a null-terminated string that represents the principal name for the server in the outbound ticket. This string should never be <b>NULL</b> when querying a security context negotiated with Kerberos.

