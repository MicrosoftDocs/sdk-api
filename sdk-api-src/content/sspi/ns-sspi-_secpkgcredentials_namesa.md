---
UID: NS:sspi._SecPkgCredentials_NamesA
title: "_SecPkgCredentials_NamesA"
author: windows-driver-content
description: The SecPkgCredentials_Names structure holds the name of the user associated with a context. The QueryCredentialsAttributes function uses this structure.
old-location: security\secpkgcredentials_names.htm
old-project: SecAuthN
ms.assetid: 38123a10-72a4-46eb-974b-3c01142dfc74
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: "*PSecPkgCredentials_NamesA, PSecPkgCredentials_Names, PSecPkgCredentials_Names structure pointer [Security], SecPkgCredentials_Names, SecPkgCredentials_Names structure [Security], SecPkgCredentials_NamesA, SecPkgCredentials_NamesW, _SecPkgCredentials_NamesA, _ssp_secpkgcredentials_names, security.secpkgcredentials_names, sspi/PSecPkgCredentials_Names, sspi/SecPkgCredentials_Names, sspi/SecPkgCredentials_NamesA, sspi/SecPkgCredentials_NamesW"
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
req.unicode-ansi: SecPkgCredentials_NamesW (Unicode) and SecPkgCredentials_NamesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SecPkgCredentials_NamesA, *PSecPkgCredentials_NamesA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Sspi.h
api_name:
-	SecPkgCredentials_Names
-	SecPkgCredentials_NamesA
-	SecPkgCredentials_NamesW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# _SecPkgCredentials_NamesA structure


## -description


The <b>SecPkgCredentials_Names</b> structure holds the name of the user associated with a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>. The 
<a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a> function uses this structure.


## -struct-fields




### -field sUserName

Pointer to a null-terminated string containing the name of the user represented by the credential. If the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> sets the SECPKG_FLAG_ACCEPT_WIN32_NAME flag to indicate that it can process Windows names, this name can be used in other Windows calls.


### -field sUserName.string

 




## -see-also




<a href="https://msdn.microsoft.com/a8ba6f73-8469-431b-b185-183b45b2c533">QueryCredentialsAttributes</a>
 

 

