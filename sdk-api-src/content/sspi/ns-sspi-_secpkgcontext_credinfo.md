---
UID: NS:sspi._SecPkgContext_CredInfo
title: "_SecPkgContext_CredInfo"
author: windows-sdk-content
description: Specifies the type of credentials used to create a client context.
old-location: security\secpkgcontext_credinfo.htm
old-project: SecAuthN
ms.assetid: 5c2c6d01-5de3-4dd1-9fa2-cce9eadd6902
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSecPkgContext_CredInfo, PSecPkgContext_CredInfo, PSecPkgContext_CredInfo structure pointer [Security], SecPkgContext_CredInfo, SecPkgContext_CredInfo structure [Security], _SecPkgContext_CredInfo, security.secpkgcontext_credinfo, sspi/PSecPkgContext_CredInfo, sspi/SecPkgContext_CredInfo"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SecPkgContext_CredInfo, *PSecPkgContext_CredInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgContext_CredInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# _SecPkgContext_CredInfo structure


## -description


Specifies the type of credentials used to create a client context.


## -struct-fields




### -field CredClass

A value of the <a href="https://msdn.microsoft.com/2f5f9be2-e7b5-4d34-a2ad-89a99db78ad0">SECPKG_CRED_CLASS</a> enumeration that indicates the type of credentials.


### -field IsPromptingNeeded

A nonzero value indicates that the application must prompt the user for credentials. All other values indicate that the application does not need to prompt the user.


## -see-also




<a href="https://msdn.microsoft.com/720b37dd-a957-4da9-8b94-4642e515bc22">SpQueryContextAttributes</a>
 

 

